---
title: IWMPSettings2 requestMediaAccessRights 方法
description: RequestMediaAccessRights 方法會要求存取程式庫的指定層級。 |IWMPSettings2 requestMediaAccessRights 方法
ms.assetid: ea33852c-d1e0-45cf-8954-2a1e2fe51910
keywords:
- requestMediaAccessRights 方法 Windows Media Player
- requestMediaAccessRights 方法 Windows Media Player，IWMPSettings2 介面
- IWMPSettings2 介面 Windows Media Player，requestMediaAccessRights 方法
topic_type:
- apiref
api_name:
- IWMPSettings2.requestMediaAccessRights
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c609afffc1d9b228d908d905e0eb1a6ef8741032
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000808"
---
# <a name="iwmpsettings2requestmediaaccessrights-method"></a><span data-ttu-id="2493d-107">IWMPSettings2：： requestMediaAccessRights 方法</span><span class="sxs-lookup"><span data-stu-id="2493d-107">IWMPSettings2::requestMediaAccessRights method</span></span>

<span data-ttu-id="2493d-108">**RequestMediaAccessRights** 方法會要求存取程式庫的指定層級。</span><span class="sxs-lookup"><span data-stu-id="2493d-108">The **requestMediaAccessRights** method requests a specified level of access to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="2493d-109">語法</span><span class="sxs-lookup"><span data-stu-id="2493d-109">Syntax</span></span>


```CSharp
public System.Boolean requestMediaAccessRights(
  System.String bstrDesiredAccess
);
```


```VB

Public Function requestMediaAccessRights( _
  ByVal bstrDesiredAccess As System.String _
) As System.Boolean
Implements IWMPSettings2.requestMediaAccessRights
```





## <a name="parameters"></a><span data-ttu-id="2493d-110">參數</span><span class="sxs-lookup"><span data-stu-id="2493d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2493d-111">*bstrDesiredAccess* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2493d-111">*bstrDesiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2493d-112">**System.string** ，這是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="2493d-112">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="2493d-113">值</span><span class="sxs-lookup"><span data-stu-id="2493d-113">Value</span></span> | <span data-ttu-id="2493d-114">描述</span><span class="sxs-lookup"><span data-stu-id="2493d-114">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="2493d-115">無</span><span class="sxs-lookup"><span data-stu-id="2493d-115">none</span></span>  | <span data-ttu-id="2493d-116">僅限目前的專案存取權限。</span><span class="sxs-lookup"><span data-stu-id="2493d-116">Current item access rights only.</span></span> |
| <span data-ttu-id="2493d-117">讀取</span><span class="sxs-lookup"><span data-stu-id="2493d-117">read</span></span>  | <span data-ttu-id="2493d-118">僅限讀取存取許可權。</span><span class="sxs-lookup"><span data-stu-id="2493d-118">Read access rights only.</span></span>         |
| <span data-ttu-id="2493d-119">完整</span><span class="sxs-lookup"><span data-stu-id="2493d-119">full</span></span>  | <span data-ttu-id="2493d-120">讀取/寫入存取權限。</span><span class="sxs-lookup"><span data-stu-id="2493d-120">Read/Write access rights.</span></span>        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2493d-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="2493d-121">Return value</span></span>

<span data-ttu-id="2493d-122">指出是否已授與所要求之存取權限的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="2493d-122">A **System.Boolean** that indicates whether the requested access rights were granted.</span></span>

## <a name="remarks"></a><span data-ttu-id="2493d-123">備註</span><span class="sxs-lookup"><span data-stu-id="2493d-123">Remarks</span></span>

<span data-ttu-id="2493d-124">網頁必須先向使用者要求許可權，以讀取或寫入文件庫中的資料。</span><span class="sxs-lookup"><span data-stu-id="2493d-124">A webpage must first request permission from the user to read information from or write data to the library.</span></span> <span data-ttu-id="2493d-125">叫用這個方法會提示使用者一個對話方塊，要求指定的許可權等級。</span><span class="sxs-lookup"><span data-stu-id="2493d-125">Invoking this method prompts the user with a dialog box that requests the specified permission level.</span></span> <span data-ttu-id="2493d-126">這表示，如果未授與適當的存取權限，就無法從程式碼存取某些方法、屬性和事件。</span><span class="sxs-lookup"><span data-stu-id="2493d-126">This means that certain methods, properties, and events will be inaccessible from code if the appropriate access rights have not been granted.</span></span> <span data-ttu-id="2493d-127">您可以使用 **IWMPSettings2 mediaAccessRights** 來抓取目前的存取權限層級。</span><span class="sxs-lookup"><span data-stu-id="2493d-127">The current access rights level can be retrieved by using **IWMPSettings2.mediaAccessRights**.</span></span>

<span data-ttu-id="2493d-128">在使用者電腦上執行的應用程式不需要使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="2493d-128">Applications running on the user's computer are not required to use this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2493d-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="2493d-129">Requirements</span></span>



| <span data-ttu-id="2493d-130">需求</span><span class="sxs-lookup"><span data-stu-id="2493d-130">Requirement</span></span> | <span data-ttu-id="2493d-131">值</span><span class="sxs-lookup"><span data-stu-id="2493d-131">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2493d-132">版本</span><span class="sxs-lookup"><span data-stu-id="2493d-132">Version</span></span><br/>   | <span data-ttu-id="2493d-133">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="2493d-133">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="2493d-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="2493d-134">Namespace</span></span><br/> | <span data-ttu-id="2493d-135">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="2493d-135">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2493d-136">組件</span><span class="sxs-lookup"><span data-stu-id="2493d-136">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2493d-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="2493d-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2493d-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2493d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2493d-139">**IWMPSettings2 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="2493d-139">**IWMPSettings2 Interface (VB and C#)**</span></span>](iwmpsettings2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2493d-140">**IWMPSettings2. mediaAccessRights (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="2493d-140">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





