---
description: 從裝置的物件樹狀結構中移除目前的 IWiaItem2 物件。
ms.assetid: 247eb36f-3e5c-4030-8334-1a4028b3eb44
title: 'IWiaItem2：:D eleteItem 方法 (Wia. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeleteItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: ef6a4204b591f06811f0941ca0ceed72b76151db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106984170"
---
# <a name="iwiaitem2deleteitem-method"></a><span data-ttu-id="51d7e-103">IWiaItem2：:D eleteItem 方法</span><span class="sxs-lookup"><span data-stu-id="51d7e-103">IWiaItem2::DeleteItem method</span></span>

<span data-ttu-id="51d7e-104">從裝置的物件樹狀結構中移除目前的 [**IWiaItem2**](-wia-iwiaitem2.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="51d7e-104">Removes the current [**IWiaItem2**](-wia-iwiaitem2.md) object from the device's object tree.</span></span>

## <a name="syntax"></a><span data-ttu-id="51d7e-105">語法</span><span class="sxs-lookup"><span data-stu-id="51d7e-105">Syntax</span></span>


```C++
HRESULT DeleteItem(
  [in] LONG lFlags
);
```



## <a name="parameters"></a><span data-ttu-id="51d7e-106">參數</span><span class="sxs-lookup"><span data-stu-id="51d7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51d7e-107">*lFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="51d7e-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51d7e-108">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="51d7e-108">Type: **LONG**</span></span>

<span data-ttu-id="51d7e-109">目前未使用。</span><span class="sxs-lookup"><span data-stu-id="51d7e-109">Currently unused.</span></span> <span data-ttu-id="51d7e-110">應該設定為零。</span><span class="sxs-lookup"><span data-stu-id="51d7e-110">Should be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51d7e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="51d7e-111">Return value</span></span>

<span data-ttu-id="51d7e-112">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="51d7e-112">Type: **HRESULT**</span></span>

<span data-ttu-id="51d7e-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="51d7e-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="51d7e-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="51d7e-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="51d7e-115">備註</span><span class="sxs-lookup"><span data-stu-id="51d7e-115">Remarks</span></span>

<span data-ttu-id="51d7e-116">Windows 映像取得 (WIA) 2.0 執行時間系統會將連接到使用者電腦的每個 WIA 2.0 硬體裝置，表示為 [**IWiaItem2**](-wia-iwiaitem2.md) 物件的階層式樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="51d7e-116">The Windows Image Acquisition (WIA) 2.0 run-time system represents each WIA 2.0 hardware device connected to the user's computer as a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="51d7e-117">指定的 WIA 2.0 裝置不一定會允許應用程式從其樹狀結構中刪除 **IWiaItem2** 物件。</span><span class="sxs-lookup"><span data-stu-id="51d7e-117">A given WIA 2.0 device may or may not allow applications to delete **IWiaItem2** objects from its tree.</span></span> <span data-ttu-id="51d7e-118">無法刪除具有子系的專案。</span><span class="sxs-lookup"><span data-stu-id="51d7e-118">Items that have children cannot be deleted.</span></span> <span data-ttu-id="51d7e-119">[**IEnumWIA \_ DEV \_ cap**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)介面必須用來查詢裝置以取得專案刪除功能。</span><span class="sxs-lookup"><span data-stu-id="51d7e-119">The [**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) interface must be used to query the device for item deletion capability.</span></span>

<span data-ttu-id="51d7e-120">如果裝置支援在其 [**IWiaItem2**](-wia-iwiaitem2.md) 樹狀目錄中刪除專案，請呼叫 **IWiaItem2：:D eleteitem** 方法以移除 **IWiaItem2** 物件。</span><span class="sxs-lookup"><span data-stu-id="51d7e-120">If the device supports item deletion in its [**IWiaItem2**](-wia-iwiaitem2.md) tree, call the **IWiaItem2::DeleteItem** method to remove the **IWiaItem2** object.</span></span> <span data-ttu-id="51d7e-121">請注意，這個方法只會在對物件的所有參考都已釋放之後刪除物件。</span><span class="sxs-lookup"><span data-stu-id="51d7e-121">Note that this method only deletes an object after all references to the object have been released.</span></span> <span data-ttu-id="51d7e-122">如果專案的刪除失敗， \_ 則會傳回 E DELETEITEM。</span><span class="sxs-lookup"><span data-stu-id="51d7e-122">If the deletion of an item has failed, E\_DELETEITEM is returned.</span></span> <span data-ttu-id="51d7e-123">尚未定義此錯誤的數值。</span><span class="sxs-lookup"><span data-stu-id="51d7e-123">The numeric value for this error is not yet defined.</span></span>

## <a name="requirements"></a><span data-ttu-id="51d7e-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="51d7e-124">Requirements</span></span>



| <span data-ttu-id="51d7e-125">需求</span><span class="sxs-lookup"><span data-stu-id="51d7e-125">Requirement</span></span> | <span data-ttu-id="51d7e-126">值</span><span class="sxs-lookup"><span data-stu-id="51d7e-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="51d7e-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="51d7e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="51d7e-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51d7e-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="51d7e-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="51d7e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="51d7e-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51d7e-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="51d7e-131">標頭</span><span class="sxs-lookup"><span data-stu-id="51d7e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="51d7e-132"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="51d7e-132"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="51d7e-133">Idl</span><span class="sxs-lookup"><span data-stu-id="51d7e-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="51d7e-134"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="51d7e-134"><dt>Wia.idl</dt></span></span> </dl> |



 

 




