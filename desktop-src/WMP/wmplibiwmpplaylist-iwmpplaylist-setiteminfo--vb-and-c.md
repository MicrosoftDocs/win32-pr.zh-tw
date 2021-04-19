---
title: IWMPPlaylist setItemInfo 方法
description: SetItemInfo 方法會設定目前播放清單之屬性的值。
ms.assetid: b3874298-8fbe-47a4-b696-cef0382aec7c
keywords:
- setItemInfo 方法 Windows Media Player
- setItemInfo 方法 Windows Media Player，IWMPPlaylist 介面
- IWMPPlaylist 介面 Windows Media Player，setItemInfo 方法
topic_type:
- apiref
api_name:
- IWMPPlaylist.setItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce882d050f1ce7839fe3589fced3a87d9052fec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990719"
---
# <a name="iwmpplaylistsetiteminfo-method"></a><span data-ttu-id="cf0de-106">IWMPPlaylist：： setItemInfo 方法</span><span class="sxs-lookup"><span data-stu-id="cf0de-106">IWMPPlaylist::setItemInfo method</span></span>

<span data-ttu-id="cf0de-107">**SetItemInfo** 方法會設定目前播放清單之屬性的值。</span><span class="sxs-lookup"><span data-stu-id="cf0de-107">The **setItemInfo** method sets the value of an attribute of the current playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf0de-108">語法</span><span class="sxs-lookup"><span data-stu-id="cf0de-108">Syntax</span></span>


```CSharp
public void setItemInfo(
  System.String bstrName,
  System.String bstrValue
);
```


```VB

Public Sub setItemInfo( _
  ByVal bstrName As System.String, _
  ByVal bstrValue As System.String _
)
Implements IWMPPlaylist.setItemInfo
```





## <a name="parameters"></a><span data-ttu-id="cf0de-109">參數</span><span class="sxs-lookup"><span data-stu-id="cf0de-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf0de-110">*bstrName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cf0de-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf0de-111">表示屬性名稱的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="cf0de-111">A **System.String** that is the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="cf0de-112">*bstrValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cf0de-112">*bstrValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf0de-113">表示屬性值的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="cf0de-113">A **System.String** that is the attribute value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf0de-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="cf0de-114">Return value</span></span>

<span data-ttu-id="cf0de-115">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="cf0de-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf0de-116">備註</span><span class="sxs-lookup"><span data-stu-id="cf0de-116">Remarks</span></span>

<span data-ttu-id="cf0de-117">在呼叫這個方法之前，您必須擁有程式庫的完整存取權。</span><span class="sxs-lookup"><span data-stu-id="cf0de-117">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="cf0de-118">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="cf0de-118">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="cf0de-119">如需使用這個屬性的範例程式碼，請參閱 [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="cf0de-119">See the [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf0de-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf0de-120">Requirements</span></span>



| <span data-ttu-id="cf0de-121">需求</span><span class="sxs-lookup"><span data-stu-id="cf0de-121">Requirement</span></span> | <span data-ttu-id="cf0de-122">值</span><span class="sxs-lookup"><span data-stu-id="cf0de-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf0de-123">版本</span><span class="sxs-lookup"><span data-stu-id="cf0de-123">Version</span></span><br/>   | <span data-ttu-id="cf0de-124">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="cf0de-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="cf0de-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="cf0de-125">Namespace</span></span><br/> | <span data-ttu-id="cf0de-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="cf0de-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="cf0de-127">組件</span><span class="sxs-lookup"><span data-stu-id="cf0de-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="cf0de-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="cf0de-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf0de-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf0de-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf0de-130">**IWMPPlaylist 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="cf0de-130">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cf0de-131">**IWMPPlaylist. getItemInfo (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="cf0de-131">**IWMPPlaylist.getItemInfo (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cf0de-132">**IWMPSettings2. mediaAccessRights (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="cf0de-132">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cf0de-133">**IWMPSettings2. requestMediaAccessRights (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="cf0de-133">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





