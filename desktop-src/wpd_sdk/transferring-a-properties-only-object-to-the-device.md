---
description: 將 Properties-Only 物件傳輸至裝置
ms.assetid: 6305cff9-c0ce-4ef5-a129-bc329b9c563f
title: 將 Properties-Only 物件傳輸至裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfefd2b910dd4ca585c82a4e50e894e5d9376cdf6334e27cee1fed10e3893a9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118026855"
---
# <a name="transferring-a-properties-only-object-to-the-device"></a>將 Properties-Only 物件傳輸至裝置

雖然上一個主題中的範例示範了如何在包含屬性和資料的裝置上建立內容，但本主題的重點在於建立僅限屬性的物件。

使用下表所述的介面來完成僅限屬性的傳輸。



| 介面                                                          | 描述                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| [**IPortableDeviceContent 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) | 提供內容特定方法的存取權。       |
| [**IPortableDeviceValues 介面**](iportabledevicevalues.md)   | 用來取出描述內容的屬性。 |



 

`TransferContactToDevice`範例應用程式的 ContentTransfer .cpp 模組中的函式會示範應用程式如何將連絡人資訊從電腦傳送至連線的裝置。 在此特定範例中，傳輸的連絡人名稱是硬式編碼的 "John Kane"，而傳輸的連絡人電話號碼一律為 "425-555-0123"。

函式所完成的第一 `TransferContactToDevice` 項工作是提示使用者在裝置上輸入父物件的物件識別碼， (將) 傳送內容。


```C++
HRESULT                             hr = S_OK;
WCHAR                               szSelection[81]        = {0};
CComPtr<IPortableDeviceValues>      pFinalObjectProperties;
CComPtr<IPortableDeviceContent>     pContent;

// Prompt user to enter an object identifier for the parent object on the device to transfer.
printf("Enter the identifer of the parent object which the contact will be transferred under.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content transfer\n");
}
```



下一步是取得 contact 屬性的抓取，當範例將新的連絡人寫入裝置時，將會使用此屬性。 連絡人屬性的抓取是由 `GetRequiredPropertiesForPropertiesOnlyContact` helper 函數所執行。


```C++
// 2) Get the properties that describe the object being created on the device

if (SUCCEEDED(hr))
{
    hr = GetRequiredPropertiesForPropertiesOnlyContact(szSelection,              // Parent to transfer the data under
                                                       &pFinalObjectProperties);  // Returned properties describing the data
    if (FAILED(hr))
    {
        printf("! Failed to get required properties needed to transfer an image file to the device, hr = 0x%lx\n", hr);
    }
}
```



此函數會將下列資料寫入 **IPortableDeviceValues** 物件。

-   裝置上連絡人父系的物件識別碼。  (這是裝置將用來儲存物件的目的地。 ) 
-   連絡人)  (的物件類型。
-   連絡人名稱 (「John Kane」 ) 的硬式編碼字串。
-   連絡人電話號碼 (「425-555-0123」 ) 的硬式編碼字串。

最後一個步驟會使用 helper 函式) 所設定的屬性，在裝置上建立僅限屬性的物件 (`GetRequiredPropertiesForPropertiesOnlyContact` 。 這是藉由呼叫 **IPortableDeviceContent：： CreateObjectWithPropertiesOnly** 方法來完成。


```C++
if (SUCCEEDED(hr))
{
    PWSTR pszNewlyCreatedObject = NULL;
    hr = pContent->CreateObjectWithPropertiesOnly(pFinalObjectProperties,    // Properties describing the object data
                                                  &pszNewlyCreatedObject);
    if (SUCCEEDED(hr))
    {
        printf("The contact was transferred to the device.\nThe newly created object's ID is '%ws'\n",pszNewlyCreatedObject);
    }

    if (FAILED(hr))
    {
        printf("! Failed to transfer contact object to the device, hr = 0x%lx\n",hr);
    }

    // Free the object identifier string returned from CreateObjectWithPropertiesOnly
    CoTaskMemFree(pszNewlyCreatedObject);
    pszNewlyCreatedObject = NULL;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IPortableDevice 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceContent 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**IPortableDeviceValues 介面**](iportabledevicevalues.md)
</dt> <dt>

[**程式設計指南**](programming-guide.md)
</dt> </dl>

 

 



