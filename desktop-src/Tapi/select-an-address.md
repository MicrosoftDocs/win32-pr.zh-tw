---
description: 下列程式碼範例示範如何使用 TAPI 物件來檢查可用的電話語音資源，以取得可處理一組指定之媒體類型需求的位址。 在此範例中，音訊和影片是必要的媒體。
ms.assetid: 8be40a87-931d-4cda-9ef7-f9c0489e0b7b
title: 選取位址
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: da41059c38328ff00271e4fa561561eecf83e1cb
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/20/2021
ms.locfileid: "106975720"
---
# <a name="select-an-address"></a><span data-ttu-id="f2aae-104">選取位址</span><span class="sxs-lookup"><span data-stu-id="f2aae-104">Select an Address</span></span>

<span data-ttu-id="f2aae-105">下列程式碼範例示範如何使用 TAPI 物件來檢查可用的電話語音資源，以取得可處理一組指定之媒體類型需求的位址。</span><span class="sxs-lookup"><span data-stu-id="f2aae-105">The following code example demonstrates use of the TAPI object to examine available telephony resources for an address that can handle a specified set of media type requirements.</span></span> <span data-ttu-id="f2aae-106">在此範例中，音訊和影片是必要的媒體。</span><span class="sxs-lookup"><span data-stu-id="f2aae-106">In this example, audio and video are the required media.</span></span>

<span data-ttu-id="f2aae-107">使用此程式碼範例之前，您必須在 [初始化 TAPI](initialize-tapi.md)中執行作業。</span><span class="sxs-lookup"><span data-stu-id="f2aae-107">Before using this code example, you must perform the operations in [Initialize TAPI](initialize-tapi.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="f2aae-108">此範例沒有適用于實際執行程式碼的錯誤檢查和發行。</span><span class="sxs-lookup"><span data-stu-id="f2aae-108">This example doesn't have the error checking and releases appropriate for production code.</span></span>

```cpp
// Declare the interfaces used to select an address.
IEnumAddress * pIEnumAddress;
ITAddress * pAddress;
ITMediaSupport * pMediaSupport;

// Use the TAPI object to enumerate available addresses.
hr = gpTapi->EnumerateAddresses( &pIEnumAddress );
// If (hr != S_OK) process the error here. 

// Locate an address that can support the media type the application needs.
while ( S_OK == pIEnumAddress->Next(1, &pAddress, NULL) )
{
    // Determine the media support.
    hr = pAddress->QueryInterface(
         IID_ITMediaSupport,
         (void **)&pMediaSupport
         );
    // If (hr != S_OK) process the error here. 

    // In this example, the required media type is already known.
    // The application can also use the address object to
    // enumerate the media supported, then choose from there.
    hr = pMediaSupport->QueryMediaType(
         TAPIMEDIATYPE_AUDIO|TAPIMEDIATYPE_VIDEO,
         &bSupport
         );
    // If (hr != S_OK) process the error here. 

    if (bSupport)
    {
        break;
    }
}
// pAddress is now a usable address.
```

## <a name="related-topics"></a><span data-ttu-id="f2aae-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="f2aae-109">Related topics</span></span>

[<span data-ttu-id="f2aae-110">ITTAPI::EnumerateAddresses</span><span class="sxs-lookup"><span data-stu-id="f2aae-110">ITTAPI::EnumerateAddresses</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses)

[<span data-ttu-id="f2aae-111">ITMediaSupport</span><span class="sxs-lookup"><span data-stu-id="f2aae-111">ITMediaSupport</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)

[<span data-ttu-id="f2aae-112">TAPIMEDIATYPE \_ 常數</span><span class="sxs-lookup"><span data-stu-id="f2aae-112">TAPIMEDIATYPE\_ Constants</span></span>](tapimediatype--constants.md)
