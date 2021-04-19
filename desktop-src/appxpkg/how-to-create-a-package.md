---
title: 如何建立應用程式套件 (C++)
description: 瞭解如何使用封裝 API 建立 Windows 應用程式的應用程式套件。
ms.assetid: FD677D75-50D5-4228-891F-73B5F40679B0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f1808ebf57d4c7125f5509db68e22b78ce949f7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "106966236"
---
# <a name="how-to-create-an-app-package-c"></a>如何建立應用程式套件 (C++)

瞭解如何使用 [封裝 API](interfaces.md)建立 Windows 應用程式的應用程式套件。

如果您想要手動建立傳統型應用程式套件，您也可以使用 MakeAppx.exe 工具來利用 [封裝 API](interfaces.md)。 如需詳細資訊，請參閱 [應用程式封裝工具 (MakeAppx.exe) ](make-appx-package--makeappx-exe-.md) 。

如果您使用 Visual Studio，建議您使用 Visual Studio 封裝嚮導來封裝您的應用程式。 如需詳細資訊，請參閱 [使用 Visual Studio 封裝 UWP 應用程式](/windows/msix/package/packaging-uwp-apps)。

## <a name="instructions"></a>指示

### <a name="step-1-create-a-package-writer"></a>步驟1：建立封裝寫入器

若要建立封裝寫入器，請呼叫 [**IAppxFactory：： CreatePackageWriter**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxfactory-createpackagewriter) 方法。 第一個參數是將寫入封裝的輸出資料流程。 第二個參數是指定封裝設定之 [**APPX \_ 封裝 \_ 設定**](/windows/desktop/api/AppxPackaging/ns-appxpackaging-appx_package_settings) 結構的指標。 第三個參數是輸出參數，會接收指向 [**IAppxPackageWriter**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxpackagewriter) 指標的指標。


```C++
#include <windows.h>
#include <shlwapi.h>
#include <AppxPackaging.h>

// We store the produced package under this file name.
const LPCWSTR OutputPackagePath = L"HelloWorld.appx";

int wmain()
{
    HRESULT hr = S_OK;

    // Specify the appropriate COM threading model
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    if (SUCCEEDED(hr))
    {
        // Create a package writer
        IAppxPackageWriter* packageWriter = NULL;

        hr = GetPackageWriter(OutputPackagePath, &packageWriter);
    }
}

//
// Creates an app package writer with default settings.
//
// Parameters:
//   outputFileName  
//     Fully qualified name of the app package (.appx file) to be created.
//   writer 
//     On success, receives the created instance of IAppxPackageWriter.
//
HRESULT GetPackageWriter(
    _In_ LPCWSTR outputFileName,
    _Outptr_ IAppxPackageWriter** writer)
{
    const LPCWSTR Sha256AlgorithmUri = L"https://www.w3.org/2001/04/xmlenc#sha256"; 
    HRESULT hr = S_OK;
    IStream* outputStream = NULL;
    IUri* hashMethod = NULL;
    APPX_PACKAGE_SETTINGS packageSettings = {0};
    IAppxFactory* appxFactory = NULL;

    // Create a stream over the output file for the package 
    hr = SHCreateStreamOnFileEx(
            outputFileName,
            STGM_CREATE | STGM_WRITE | STGM_SHARE_EXCLUSIVE,
            0,     // default file attributes
            TRUE,  // create file if it does not exist
            NULL,  // no template
            &outputStream);

    // Create default package writer settings, including hash algorithm URI
    // and Zip format.
    if (SUCCEEDED(hr))
    {        hr = CreateUri(
                Sha256AlgorithmUri,
                Uri_CREATE_CANONICALIZE,
                0, // reserved parameter
                &hashMethod);
    }

    if (SUCCEEDED(hr))
    {
        packageSettings.forceZip32 = TRUE;
        packageSettings.hashMethod = hashMethod;
    }

    // Create a new Appx factory
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(
                __uuidof(AppxFactory),
                NULL,
                CLSCTX_INPROC_SERVER,
                __uuidof(IAppxFactory),
                (LPVOID*)(&appxFactory));
    }

    // Create a new package writer using the factory
    if (SUCCEEDED(hr))
    {
        hr = appxFactory->CreatePackageWriter(
                outputStream,
                &packageSettings,
                writer);
    }

    // Clean up allocated resources
    if (appxFactory != NULL)
    {
        appxFactory->Release();
        appxFactory = NULL;
    }
    if (hashMethod != NULL)
    {
        hashMethod->Release();
        hashMethod = NULL;
    }
    if (outputStream != NULL)
    {
        outputStream->Release();
        outputStream = NULL;
    }
    return hr;
}
```



### <a name="step-2-add-the-payload-files-for-your-app-to-the-package"></a>步驟2：將應用程式的承載檔新增至套件

呼叫 [**IAppxPackageWriter：： AddPayloadFile**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxpackagewriter-addpayloadfile) 方法，將檔案加入封裝中。 第一個參數是檔案的相對路徑。 第二個參數表示檔案的內容類型。 第三個參數指定了 [**APPX \_ 壓縮 \_ 選項**](/windows/desktop/api/AppxPackaging/ne-appxpackaging-appx_compression_option) 列舉的選項。 第四個參數是檔案的輸入資料流程。


```C++
// Path where all input files are stored
const LPCWSTR DataPath = L"Data\\";

// Add all payload files to the package writer
for (int i = 0; SUCCEEDED(hr) && (i < PayloadFilesCount); i++)
{
    IStream* fileStream = NULL;

    hr = GetFileStream(DataPath, PayloadFilesName[i], &fileStream);

    if (SUCCEEDED(hr))
    {
        packageWriter->AddPayloadFile(
            PayloadFilesName[i],
            PayloadFilesContentType[i],
            PayloadFilesCompression[i],
            fileStream);
        }

        if (fileStream != NULL)
        {
            fileStream->Release();
            fileStream = NULL;
        }
    }
}
```



先前的程式碼會使用這些變數定義和 `GetFileStream` helper 函數。


```C++
#include <strsafe.h>
#include <shlwapi.h>

// The produced app package's content consists of these files, with
// corresponding content types and compression options.
const int PayloadFilesCount = 4;
const LPCWSTR PayloadFilesName[PayloadFilesCount] = {
    L"AppTile.png",
    L"Default.html",
    L"images\\smiley.jpg",
    L"Error.html",
};
const LPCWSTR PayloadFilesContentType[PayloadFilesCount] = {
    L"image/png",
    L"text/html",
    L"image/jpeg",
    L"text/html",
};
const APPX_COMPRESSION_OPTION PayloadFilesCompression[PayloadFilesCount] = {
    APPX_COMPRESSION_OPTION_NONE,
    APPX_COMPRESSION_OPTION_NORMAL,
    APPX_COMPRESSION_OPTION_NONE,
    APPX_COMPRESSION_OPTION_NORMAL,
};

//
// Creates a readable IStream over the specified file. For simplicity, we assume that the fully 
// qualified file name is 100 characters or less. Your code should 
// handle longer names, and allocate the buffer dynamically.
//
// Parameters:
//   path 
//      Path of the folder that contains the file to be opened; must end with a '\'
//   fileName 
//      Name, of the file to be opened, not including the path
//   stream 
//      On success, receives the created instance of IStream
//
HRESULT GetFileStream(
    _In_ LPCWSTR path,
    _In_ LPCWSTR fileName,
    _Outptr_ IStream** stream)
{
    HRESULT hr = S_OK;
    const int MaxFileNameLength = 100;
    WCHAR fullFileName[MaxFileNameLength + 1];

    // Create full file name by concatenating path and fileName
    hr = StringCchCopyW(fullFileName, MaxFileNameLength, path);
    if (SUCCEEDED(hr))
    {
        hr = StringCchCat(fullFileName, MaxFileNameLength, fileName);
    }

    // Create stream for reading the file
    if (SUCCEEDED(hr))
    {
        hr = SHCreateStreamOnFileEx(
                fullFileName,
                STGM_READ | STGM_SHARE_EXCLUSIVE,
                0,      // default file attributes
                FALSE,  // don't create new file
                NULL,   // no template
                stream);
    }
    return hr;
}
```



### <a name="step-3-add-the-package-manifest-to-the-package"></a>步驟3：將套件資訊清單新增至套件

每個封裝都必須有套件資訊清單。 若要將封裝資訊清單加入封裝中，請建立檔案的輸入資料流程，然後呼叫 [**IAppxPackageWriter：： Close**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxpackagewriter-close) 方法，在封裝結尾寫入資訊清單，並關閉封裝寫入器的輸出資料流程。

此程式碼會使用 `GetFileStream` 上一個步驟中所示的 helper 函式來建立封裝資訊清單的資料流程。


```C++
// We read the app package's manifest from this file
const LPCWSTR ManifestFileName = L"AppxManifest.xml";

IStream* manifestStream = NULL;

hr = GetFileStream(DataPath, ManifestFileName, &manifestStream);

if (SUCCEEDED(hr))
{
    hr = packageWriter->Close(manifestStream);
}

if (manifestStream != NULL)
{
    manifestStream->Release();
    manifestStream = NULL;
}
```



### <a name="step-4-clean-up-the-package-writer"></a>步驟4：清除封裝寫入器

從函式傳回之前 `wmain` ，呼叫 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 方法以清除封裝寫入器並呼叫 [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) 函數。


```C++
if (packageWriter != NULL)
{
    packageWriter->Release();
    packageWriter = NULL;
}
CoUninitialize();
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**範例**
</dt> <dt>

[建立應用程式套件範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

**參考**
</dt> <dt>

[**IAppxPackageWriter**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxpackagewriter)
</dt> </dl>

 

 