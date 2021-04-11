---
description: 應用程式會使用裝置的 IWiaPropertyStorage 介面來讀取和寫入裝置屬性。 IWiaPropertyStorage 會繼承元件物件模型的所有方法， (COM) 介面 IPropertyStorage。
ms.assetid: 65ca9e71-9a0f-495f-b78c-3b1a8d66ee33
title: 讀取裝置屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235ba701ed3356e09070709f3c99f2826c69c8c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943461"
---
# <a name="reading-device-properties"></a><span data-ttu-id="74cbc-104">讀取裝置屬性</span><span class="sxs-lookup"><span data-stu-id="74cbc-104">Reading Device Properties</span></span>

<span data-ttu-id="74cbc-105">應用程式會使用裝置的 [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) 介面來讀取和寫入裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="74cbc-105">Applications use a device's [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface to read and write device properties.</span></span> <span data-ttu-id="74cbc-106">**IWiaPropertyStorage** 會繼承元件物件模型的所有方法， (COM) 介面 [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage)。</span><span class="sxs-lookup"><span data-stu-id="74cbc-106">**IWiaPropertyStorage** inherits all of the methods of the Component Object Model (COM) interface [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage).</span></span>

<span data-ttu-id="74cbc-107">裝置屬性包含描述裝置功能和設定之裝置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="74cbc-107">Device properties include information about a device that describe the device's capabilities and settings.</span></span> <span data-ttu-id="74cbc-108">如需這些屬性的清單，請參閱 [裝置屬性](-wia-device-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="74cbc-108">For a list of these properties, see [Device Properties](-wia-device-properties.md).</span></span>

<span data-ttu-id="74cbc-109">使用 [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) 讀取的裝置屬性是裝置識別碼，然後用來建立 Windows 映像取得 (WIA) 裝置。</span><span class="sxs-lookup"><span data-stu-id="74cbc-109">Among the device properties that are read using [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) is the device ID, that is then used to create a Windows Image Acquisition (WIA) device.</span></span> <span data-ttu-id="74cbc-110">如需詳細資訊，請參閱 [**IWiaDevMgr：： CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (或 [**IWiaDevMgr2：： CreateDevice**](-wia-iwiadevmgr2-createdevice.md)) 。</span><span class="sxs-lookup"><span data-stu-id="74cbc-110">For more information, see [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (or [**IWiaDevMgr2::CreateDevice**](-wia-iwiadevmgr2-createdevice.md)).</span></span>

<span data-ttu-id="74cbc-111">下列範例會從裝置屬性的陣列讀取裝置識別碼、裝置名稱和裝置描述，並將這些屬性列印至主控台。</span><span class="sxs-lookup"><span data-stu-id="74cbc-111">The following example reads the device ID, the device name, and the device description from the array of device properties, and prints these properties to the console.</span></span>


```
    HRESULT ReadSomeWiaProperties( IWiaPropertyStorage *pWiaPropertyStorage )
    {
        //
        // Validate arguments
        //
        if (NULL == pWiaPropertyStorage)
        {
            return E_INVALIDARG;
        }

        //
        // Declare PROPSPECs and PROPVARIANTs, and initialize them to zero.
        //
        PROPSPEC PropSpec[3] = {0};
        PROPVARIANT PropVar[3] = {0};

        //
        // How many properties are you querying for?
        //
        const ULONG c_nPropertyCount = sizeof(PropSpec)/sizeof(PropSpec[0]);

        //
        // Define which properties you want to read:
        // Device ID.  This is what you would use to create
        // the device.
        //
        PropSpec[0].ulKind = PRSPEC_PROPID;
        PropSpec[0].propid = WIA_DIP_DEV_ID;

        //
        // Device Name
        //
        PropSpec[1].ulKind = PRSPEC_PROPID;
        PropSpec[1].propid = WIA_DIP_DEV_NAME;

        //
        // Device description
        //
        PropSpec[2].ulKind = PRSPEC_PROPID;
        PropSpec[2].propid = WIA_DIP_DEV_DESC;

        //
        // Ask for the property values
        //
        HRESULT hr = pWiaPropertyStorage->ReadMultiple( c_nPropertyCount, PropSpec, PropVar );
        if (SUCCEEDED(hr))
        {
            //
            // IWiaPropertyStorage::ReadMultiple will return S_FALSE if some
            // properties could not be read, so you have to check the return
            // types for each requested item.
            //

            //
            // Check the return type for the device ID
            //
            if (VT_BSTR == PropVar[0].vt)
            {
                //
                // Do something with the device ID
                //
                _tprintf( TEXT("WIA_DIP_DEV_ID: %ws\n"), PropVar[0].bstrVal );
            }

            //
            // Check the return type for the device name
            //
            if (VT_BSTR == PropVar[1].vt)
            {
                //
                // Do something with the device name
                //
                _tprintf( TEXT("WIA_DIP_DEV_NAME: %ws\n"), PropVar[1].bstrVal );
            }

            //
            // Check the return type for the device description
            //
            if (VT_BSTR == PropVar[2].vt)
            {
                //
                // Do something with the device description
                //
                _tprintf( TEXT("WIA_DIP_DEV_DESC: %ws\n"), PropVar[2].bstrVal );
            }

            //
            // Free the returned PROPVARIANTs
            //
            FreePropVariantArray( c_nPropertyCount, PropVar );
        }

        //
        // Return the result of reading the properties
        //
        return hr;
    }
```



<span data-ttu-id="74cbc-112">在此範例中，應用程式會) 分別 (**PropSpec** 和 **PropVar** 設定 [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)陣列，以保存屬性資訊。</span><span class="sxs-lookup"><span data-stu-id="74cbc-112">In this example, the application sets up [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) arrays (**PropSpec** and **PropVar**, respectively) to hold property information.</span></span> <span data-ttu-id="74cbc-113">在 [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)指標 **pIWiaPropStg** 的 [IPropertyStorage：： ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple)方法呼叫中，會以參數的形式傳遞這些陣列。</span><span class="sxs-lookup"><span data-stu-id="74cbc-113">These arrays are passed as parameters in the call to [IPropertyStorage::ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) method of the [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) pointer **pIWiaPropStg**.</span></span> <span data-ttu-id="74cbc-114">**PropSpec** 陣列的每個元素都包含裝置屬性的類型和名稱。</span><span class="sxs-lookup"><span data-stu-id="74cbc-114">Each element of the **PropSpec** array contains the type and name of a device property.</span></span> <span data-ttu-id="74cbc-115">傳回時， **PropVar** 的每個元素都會包含由 **PropSpec** 陣列的對應元素所代表的裝置屬性值。</span><span class="sxs-lookup"><span data-stu-id="74cbc-115">Upon return, each element of the **PropVar** contains the value of the device property represented by the corresponding element of the **PropSpec** array.</span></span>

<span data-ttu-id="74cbc-116">然後，應用程式會呼叫 [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)指標 **pWiaPropertyStorage** 的 [IPropertyStorage：： ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple)屬性，以取得屬性資訊。</span><span class="sxs-lookup"><span data-stu-id="74cbc-116">The application then calls [IPropertyStorage::ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) property of the [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) pointer **pWiaPropertyStorage** to retrieve the property information.</span></span>

<span data-ttu-id="74cbc-117">用來讀取和設定裝置屬性的技術與專案屬性相同，唯一的差別是您呼叫適當方法的 WIA 專案類型。</span><span class="sxs-lookup"><span data-stu-id="74cbc-117">The technique used to read and set device properties is the same as that for item properties, the only difference is the type of the WIA item on which you call the appropriate methods.</span></span> <span data-ttu-id="74cbc-118">如需專案屬性的清單，請參閱 [專案屬性](-wia-item-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="74cbc-118">For a list of item properties, see [Item Properties](-wia-item-properties.md).</span></span>

 

 
