---
description: 取得專案的類別目錄資訊。
ms.assetid: 4d6f7a6a-280d-4b36-8e1d-8d9fcaa8a1de
title: 'IWiaItem2：： GetItemCategory 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetItemCategory
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: fdf650e8b540fcb9dc58f93f34771462fbc0a5c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971012"
---
# <a name="iwiaitem2getitemcategory-method"></a><span data-ttu-id="4fc60-103">IWiaItem2：： GetItemCategory 方法</span><span class="sxs-lookup"><span data-stu-id="4fc60-103">IWiaItem2::GetItemCategory method</span></span>

<span data-ttu-id="4fc60-104">取得專案的類別目錄資訊。</span><span class="sxs-lookup"><span data-stu-id="4fc60-104">Gets an item's category information.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fc60-105">語法</span><span class="sxs-lookup"><span data-stu-id="4fc60-105">Syntax</span></span>


```C++
HRESULT GetItemCategory(
  [out] GUID *pItemCategoryGUID
);
```



## <a name="parameters"></a><span data-ttu-id="4fc60-106">參數</span><span class="sxs-lookup"><span data-stu-id="4fc60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fc60-107">*pItemCategoryGUID* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4fc60-107">*pItemCategoryGUID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4fc60-108">類型： \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="4fc60-108">Type: \**GUID\** _</span></span>

<span data-ttu-id="4fc60-109">接收識別專案類別之 GUID 的指標。</span><span class="sxs-lookup"><span data-stu-id="4fc60-109">Receives a pointer to the GUID that identifies the category of the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fc60-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="4fc60-110">Return value</span></span>

<span data-ttu-id="4fc60-111">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="4fc60-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="4fc60-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="4fc60-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4fc60-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4fc60-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fc60-114">備註</span><span class="sxs-lookup"><span data-stu-id="4fc60-114">Remarks</span></span>

<span data-ttu-id="4fc60-115">與 Windows 映像取得相關聯之物件的階層式樹狀結構中的每個 [**IWiaItem2**](-wia-iwiaitem2.md) 物件 (WIA) 2.0 硬體裝置都有特定的類別。</span><span class="sxs-lookup"><span data-stu-id="4fc60-115">Every [**IWiaItem2**](-wia-iwiaitem2.md) object in the hierarchical tree of objects associated with a Windows Image Acquisition (WIA) 2.0 hardware device has a specific category.</span></span> <span data-ttu-id="4fc60-116">此方法可讓應用程式識別裝置中專案物件階層式樹狀結構中任何專案的類別。</span><span class="sxs-lookup"><span data-stu-id="4fc60-116">This method enables applications to identify the category of any item in a hierarchical tree of item objects in a device.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fc60-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="4fc60-117">Requirements</span></span>



| <span data-ttu-id="4fc60-118">需求</span><span class="sxs-lookup"><span data-stu-id="4fc60-118">Requirement</span></span> | <span data-ttu-id="4fc60-119">值</span><span class="sxs-lookup"><span data-stu-id="4fc60-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4fc60-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4fc60-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4fc60-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4fc60-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4fc60-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4fc60-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4fc60-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4fc60-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4fc60-124">標頭</span><span class="sxs-lookup"><span data-stu-id="4fc60-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fc60-125"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="4fc60-125"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="4fc60-126">Idl</span><span class="sxs-lookup"><span data-stu-id="4fc60-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4fc60-127"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="4fc60-127"><dt>Wia.idl</dt></span></span> </dl> |



 

 




