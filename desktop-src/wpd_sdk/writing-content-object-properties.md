---
description: 撰寫物件屬性
ms.assetid: f762a571-83ea-4999-ad49-a51044bc790d
title: 撰寫物件屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 726501c986e73033437de3bee0c11b3beb66150d
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423928"
---
# <a name="writing-object-properties"></a><span data-ttu-id="5110c-103">撰寫物件屬性</span><span class="sxs-lookup"><span data-stu-id="5110c-103">Writing Object Properties</span></span>

<span data-ttu-id="5110c-104">服務通常會包含屬於每個服務支援之其中一種格式的子物件。</span><span class="sxs-lookup"><span data-stu-id="5110c-104">Services often contain child objects that belong to one of the formats that each service supports.</span></span> <span data-ttu-id="5110c-105">例如，「連絡人」服務可能支援「抽象連絡人」格式的多個連絡人物件。</span><span class="sxs-lookup"><span data-stu-id="5110c-105">For example, a Contacts service may support multiple contact objects of the Abstract Contact format.</span></span> <span data-ttu-id="5110c-106">每個連絡人物件都是由相關屬性描述 (連絡人名稱、電話號碼、電子郵件地址等) 。</span><span class="sxs-lookup"><span data-stu-id="5110c-106">Each contact object is described by related properties (contact name, phone number, email address, and so on).</span></span>

<span data-ttu-id="5110c-107">WpdServicesApiSample 應用程式包含的程式碼會示範應用程式如何更新指定連絡人服務之子物件的 name 屬性。</span><span class="sxs-lookup"><span data-stu-id="5110c-107">The WpdServicesApiSample application includes code that demonstrates how an application can update the name property for a child object of the given Contacts service.</span></span> <span data-ttu-id="5110c-108">此範例會使用下列 WPD 介面。</span><span class="sxs-lookup"><span data-stu-id="5110c-108">This sample uses the following WPD interfaces.</span></span>



| <span data-ttu-id="5110c-109">介面</span><span class="sxs-lookup"><span data-stu-id="5110c-109">Interface</span></span>                                                      | <span data-ttu-id="5110c-110">描述</span><span class="sxs-lookup"><span data-stu-id="5110c-110">Description</span></span>                                                                                                                                                          |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5110c-111">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="5110c-111">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)       | <span data-ttu-id="5110c-112">用來取出 **IPortableDeviceContent2** 介面，以存取支援的服務方法。</span><span class="sxs-lookup"><span data-stu-id="5110c-112">Used to retrieve the **IPortableDeviceContent2** interface to access the supported service methods.</span></span>                                                                  |
| [<span data-ttu-id="5110c-113">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="5110c-113">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)     | <span data-ttu-id="5110c-114">提供內容特定方法的存取權。</span><span class="sxs-lookup"><span data-stu-id="5110c-114">Provides access to the content-specific methods.</span></span>                                                                                                                     |
| [<span data-ttu-id="5110c-115">**IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="5110c-115">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) | <span data-ttu-id="5110c-116">用來寫入物件屬性值，並判斷是否可以撰寫指定的屬性</span><span class="sxs-lookup"><span data-stu-id="5110c-116">Used to write the object property values and to determine whether a given property can be written</span></span>                                                                    |
| [<span data-ttu-id="5110c-117">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="5110c-117">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)         | <span data-ttu-id="5110c-118">用來保存要寫入的屬性值、判斷寫入作業的結果，以及在決定寫入功能) 時， (抓取屬性的屬性。</span><span class="sxs-lookup"><span data-stu-id="5110c-118">Used to hold the property values to be written, determine results of the write operation, and retrieve attributes of properties (when determining write capability).</span></span> |



 

<span data-ttu-id="5110c-119">當使用者在命令列選擇選項 "8" 時，應用程式會叫用在 ContentProperties .cpp 模組中找到的 **WriteContentProperties** 方法。</span><span class="sxs-lookup"><span data-stu-id="5110c-119">When the user chooses option "8" at the command line, the application invokes the **WriteContentProperties** method that is found in the ContentProperties.cpp module.</span></span> <span data-ttu-id="5110c-120">這個方法會提示使用者輸入要更新之屬性的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="5110c-120">This method prompts the user to enter an object identifier for the property to be updated.</span></span> <span data-ttu-id="5110c-121">使用者識別物件，且該方法會提示使用者指定新的名稱。</span><span class="sxs-lookup"><span data-stu-id="5110c-121">The user identifies the object, and the method prompts the user to specify a new name.</span></span> <span data-ttu-id="5110c-122">指定此名稱之後，方法會更新指定之物件的 Name 屬性。</span><span class="sxs-lookup"><span data-stu-id="5110c-122">After this name is specified, the method updates the Name property for the given object.</span></span>

<span data-ttu-id="5110c-123">請注意，在撰寫物件屬性之前，範例應用程式會在連線的裝置上開啟連絡人服務。</span><span class="sxs-lookup"><span data-stu-id="5110c-123">Note that prior to writing the object properties, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="5110c-124">下列 **WriteContentProperties** 方法的程式碼會示範應用程式如何使用 [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) 介面來取出 [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) 介面。</span><span class="sxs-lookup"><span data-stu-id="5110c-124">The following code for the **WriteContentProperties** method demonstrates how the application uses the [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) interface to retrieve an [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) interface.</span></span> <span data-ttu-id="5110c-125">藉由將要求的屬性 PROPERTYKEYS 傳遞至 [**IPortableDeviceProperties：： SetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) 方法， **WriteContentProperties** 會更新 name 屬性。</span><span class="sxs-lookup"><span data-stu-id="5110c-125">By passing the PROPERTYKEYS of the requested properties to the [**IPortableDeviceProperties::SetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method, **WriteContentProperties** updates the name property.</span></span>


```C++
void WriteContentProperties(
 IPortableDeviceService* pService)
{
 if (pService == NULL)
 {
  printf("! A NULL IPortableDeviceService interface pointer was received\n");
  return;
 }

 HRESULT          hr       = S_OK;
 WCHAR         wszSelection[81]  = {0};
 WCHAR         wszNewObjectName[81] = {0};
 CComPtr<IPortableDeviceProperties> pProperties;
 CComPtr<IPortableDeviceContent2>   pContent;
 CComPtr<IPortableDeviceValues>  pObjectPropertiesToWrite;
 CComPtr<IPortableDeviceValues>  pPropertyWriteResults;
 CComPtr<IPortableDeviceValues>  pAttributes;
 BOOL          bCanWrite   = FALSE;

 // Prompt user to enter an object identifier on the device to write properties on.
 printf("Enter the identifer of the object you wish to write properties on.\n>");
 hr = StringCbGetsW(wszSelection,sizeof(wszSelection));
 if (FAILED(hr))
 {
  printf("An invalid object identifier was specified, aborting property reading\n");
 }

 // 1) Get an IPortableDeviceContent2 interface from the IPortableDeviceService interface to
 // access the content-specific methods.
 if (SUCCEEDED(hr))
 {
  hr = pService->Content(&pContent);
  if (FAILED(hr))
  {
   printf("! Failed to get IPortableDeviceContent2 from IPortableDeviceService, hr = 0x%lx\n",hr);
  }
 }

 // 2) Get an IPortableDeviceProperties interface from the IPortableDeviceContent2 interface
 // to access the property-specific methods.
 if (SUCCEEDED(hr))
 {
  hr = pContent->Properties(&pProperties);
  if (FAILED(hr))
  {
   printf("! Failed to get IPortableDeviceProperties from IPortableDeviceContent2, hr = 0x%lx\n",hr);
  }
 }

 // 3) Check the property attributes to see if we can write/change the NAME_GenericObj_Name property.
 if (SUCCEEDED(hr))
 {
  hr = pProperties->GetPropertyAttributes(wszSelection,
            PKEY_GenericObj_Name,
            &pAttributes);
  if (SUCCEEDED(hr))
  {
   hr = pAttributes->GetBoolValue(WPD_PROPERTY_ATTRIBUTE_CAN_WRITE, &bCanWrite);
   if (SUCCEEDED(hr))
   {
    if (bCanWrite)
    {
     printf("The attribute WPD_PROPERTY_ATTRIBUTE_CAN_WRITE for PKEY_GenericObj_Name reports TRUE\nThis means that the property can be changed/updated\n\n");
    }
    else
    {
     printf("The attribute WPD_PROPERTY_ATTRIBUTE_CAN_WRITE for PKEY_GenericObj_Name reports FALSE\nThis means that the property cannot be changed/updated\n\n");
    }
   }
   else
   {
    printf("! Failed to get the WPD_PROPERTY_ATTRIBUTE_CAN_WRITE value for PKEY_GenericObj_Name on object '%ws', hr = 0x%lx\n", wszSelection, hr);
   }
  }
 }

 // 4) Prompt the user for the new value of the NAME_GenericObj_Name property only if the property attributes report
 // that it can be changed/updated.
 if (bCanWrite)
 {
  printf("Enter the new PKEY_GenericObj_Name property for the object '%ws'.\n>",wszSelection);
  hr = StringCbGetsW(wszNewObjectName,sizeof(wszNewObjectName));
  if (FAILED(hr))
  {
   printf("An invalid PKEY_GenericObj_Name was specified, aborting property writing\n");
  }

  // 5) CoCreate an IPortableDeviceValues interface to hold the property values
  // we wish to write.
  if (SUCCEEDED(hr))
  {
   hr = CoCreateInstance(CLSID_PortableDeviceValues,
          NULL,
          CLSCTX_INPROC_SERVER,
          IID_IPortableDeviceValues,
          (VOID**) &pObjectPropertiesToWrite);
   if (SUCCEEDED(hr))
   {
    if (pObjectPropertiesToWrite != NULL)
    {
     hr = pObjectPropertiesToWrite->SetStringValue(PKEY_GenericObj_Name, wszNewObjectName);
     if (FAILED(hr))
     {
      printf("! Failed to add PKEY_GenericObj_Name to IPortableDeviceValues, hr= 0x%lx\n", hr);
     }
    }
   }
  }

  // 6) Call SetValues() passing the collection of specified PROPERTYKEYs.
  if (SUCCEEDED(hr))
  {
   hr = pProperties->SetValues(wszSelection,      // The object whose properties we are reading
          pObjectPropertiesToWrite,   // The properties we want to read
          &pPropertyWriteResults); // Driver supplied property result values for the property read operation
   if (FAILED(hr))
   {
    printf("! Failed to set properties for object '%ws', hr= 0x%lx\n", wszSelection, hr);
   }
   else
   {
    printf("The PKEY_GenericObj_Name property on object '%ws' was written successfully (Read the properties again to see the updated value)\n", wszSelection);
   }
  }
 }
}
```



## <a name="related-topics"></a><span data-ttu-id="5110c-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="5110c-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5110c-127">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="5110c-127">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[<span data-ttu-id="5110c-128">**IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="5110c-128">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="5110c-129">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="5110c-129">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



