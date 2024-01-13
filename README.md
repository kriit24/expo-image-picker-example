# expo-image-picker-example


`
let requestPermission = await ImagePicker.requestCameraPermissionsAsync();

if (requestPermission.granted === false) {
    alert('Permission to access image roll is required!');
    return;
}

let result = await ImagePicker.launchCameraAsync({
    mediaTypes: ImagePicker.MediaTypeOptions.All,
    quality: 0.4,
    allowsEditing: false,
    base64: true,
});

if (!result.canceled) {
    let filename = result.assets[0].uri.substring(
        result.assets[0].uri.lastIndexOf('/') + 1,
        result.assets[0].uri.length
    );

    console.log(filename);
}
`
