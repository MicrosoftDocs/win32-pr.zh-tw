---
title: IWMPSettings2 mediaAccessRights 屬性
description: MediaAccessRights 屬性會取得值，指出目前授與存取程式庫的許可權。
ms.assetid: c4289a2c-e343-405d-9bf5-0e97f6617916
keywords:
- mediaAccessRights 屬性 Windows Media Player
- mediaAccessRights 屬性 Windows Media Player，IWMPSettings2 介面
- IWMPSettings2 介面 Windows Media Player，mediaAccessRights 屬性
topic_type:
- apiref
api_name:
- IWMPSettings2.mediaAccessRights
- IWMPSettings2.get_mediaAccessRights
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96cca06b9618767e7748b4b1308ed97860c7c80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991512"
---
# <a name="iwmpsettings2mediaaccessrights-property"></a><span data-ttu-id="fe52b-106">IWMPSettings2：： mediaAccessRights 屬性</span><span class="sxs-lookup"><span data-stu-id="fe52b-106">IWMPSettings2::mediaAccessRights property</span></span>

<span data-ttu-id="fe52b-107">**MediaAccessRights** 屬性會取得值，指出目前授與存取程式庫的許可權。</span><span class="sxs-lookup"><span data-stu-id="fe52b-107">The **mediaAccessRights** property gets a value indicating the permissions currently granted for library access.</span></span>

<span data-ttu-id="fe52b-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="fe52b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe52b-109">語法</span><span class="sxs-lookup"><span data-stu-id="fe52b-109">Syntax</span></span>


```CSharp
public System.String mediaAccessRights {get;}
```


```VB

Public ReadOnly Property mediaAccessRights As System.String
```





## <a name="property-value"></a><span data-ttu-id="fe52b-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="fe52b-110">Property value</span></span>

<span data-ttu-id="fe52b-111">**System.string** ，這是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="fe52b-111">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="fe52b-112">值</span><span class="sxs-lookup"><span data-stu-id="fe52b-112">Value</span></span> | <span data-ttu-id="fe52b-113">描述</span><span class="sxs-lookup"><span data-stu-id="fe52b-113">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="fe52b-114">無</span><span class="sxs-lookup"><span data-stu-id="fe52b-114">none</span></span>  | <span data-ttu-id="fe52b-115">僅限目前的專案存取權限。</span><span class="sxs-lookup"><span data-stu-id="fe52b-115">Current item access rights only.</span></span> |
| <span data-ttu-id="fe52b-116">讀取</span><span class="sxs-lookup"><span data-stu-id="fe52b-116">read</span></span>  | <span data-ttu-id="fe52b-117">僅限讀取存取許可權。</span><span class="sxs-lookup"><span data-stu-id="fe52b-117">Read access rights only.</span></span>         |
| <span data-ttu-id="fe52b-118">完整</span><span class="sxs-lookup"><span data-stu-id="fe52b-118">full</span></span>  | <span data-ttu-id="fe52b-119">讀取/寫入存取權限。</span><span class="sxs-lookup"><span data-stu-id="fe52b-119">Read/Write access rights.</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="fe52b-120">備註</span><span class="sxs-lookup"><span data-stu-id="fe52b-120">Remarks</span></span>

<span data-ttu-id="fe52b-121">網頁必須先向使用者要求許可權，以讀取或寫入文件庫中的資料。</span><span class="sxs-lookup"><span data-stu-id="fe52b-121">A webpage must first request permission from the user to read information from or write data to the library.</span></span> <span data-ttu-id="fe52b-122">這表示，如果未授與適當的存取權限，就無法從程式碼存取某些方法、屬性和事件。</span><span class="sxs-lookup"><span data-stu-id="fe52b-122">This means that certain methods, properties, and events will be inaccessible from code if the appropriate access rights have not been granted.</span></span> <span data-ttu-id="fe52b-123">為了取得存取權限，應用程式會呼叫 **IWMPSettings2， \_** 並傳遞指定所需存取權限層級的參數。</span><span class="sxs-lookup"><span data-stu-id="fe52b-123">To obtain access rights, the application calls **IWMPSettings2.get\_requestMediaAccessRights**, passing a parameter that specifies the desired access rights level.</span></span>

<span data-ttu-id="fe52b-124">在使用者電腦上執行的應用程式一律具有完整存取權限。</span><span class="sxs-lookup"><span data-stu-id="fe52b-124">Applications running on the user's computer always have full access rights.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe52b-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe52b-125">Requirements</span></span>



| <span data-ttu-id="fe52b-126">需求</span><span class="sxs-lookup"><span data-stu-id="fe52b-126">Requirement</span></span> | <span data-ttu-id="fe52b-127">值</span><span class="sxs-lookup"><span data-stu-id="fe52b-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe52b-128">版本</span><span class="sxs-lookup"><span data-stu-id="fe52b-128">Version</span></span><br/>   | <span data-ttu-id="fe52b-129">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="fe52b-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="fe52b-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="fe52b-130">Namespace</span></span><br/> | <span data-ttu-id="fe52b-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="fe52b-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="fe52b-132">組件</span><span class="sxs-lookup"><span data-stu-id="fe52b-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="fe52b-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="fe52b-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe52b-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe52b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe52b-135">**IWMPSettings2 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="fe52b-135">**IWMPSettings2 Interface (VB and C#)**</span></span>](iwmpsettings2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fe52b-136">**IWMPSettings2. requestMediaAccessRights (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="fe52b-136">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





