# making-QR-Code
#installing QR code library using pip
pip install qrcode

#importing QR Code
import qrcode

# Replace this with your video URL
video_url = "https://youtu.be/ePOglweqy7o?si=NbgiqOfjFnak4VkU"

# Generate QR Code
qr = qrcode.QRCode(
    version=1,
    error_correction=qrcode.constants.ERROR_CORRECT_L,
    box_size=10,
    border=4,
)

qr.add_data(video_url)
qr.make(fit=True)

# Create an image from the QR Code instance
img = qr.make_image(fill_color="black", back_color="white")
# Save the image
img.save("video_qr_code.png")

print("QR Code generated and saved as video_qr_code.png")
