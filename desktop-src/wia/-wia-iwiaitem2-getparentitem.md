---
description: 取得樹狀結構中代表 Windows 映像取得 (WIA) 2.0 硬體裝置的父專案。
ms.assetid: c6fdaf1d-9875-4852-893c-813894d89f6c
title: 'IWiaItem2：： GetParentItem 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetParentItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 055625b98807103c3b79109216f6081d00564b15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318443"
---
# <a name="iwiaitem2getparentitem-method"></a><span data-ttu-id="1aee4-103">IWiaItem2：： GetParentItem 方法</span><span class="sxs-lookup"><span data-stu-id="1aee4-103">IWiaItem2::GetParentItem method</span></span>

<span data-ttu-id="1aee4-104">取得樹狀結構中代表 Windows 映像取得 (WIA) 2.0 硬體裝置的父專案。</span><span class="sxs-lookup"><span data-stu-id="1aee4-104">Gets the parent item in the tree that represents a Windows Image Acquisition (WIA) 2.0 hardware device.</span></span>

## <a name="syntax"></a><span data-ttu-id="1aee4-105">語法</span><span class="sxs-lookup"><span data-stu-id="1aee4-105">Syntax</span></span>


```C++
HRESULT GetParentItem(
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="1aee4-106">參數</span><span class="sxs-lookup"><span data-stu-id="1aee4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1aee4-107">*ppIWiaItem2* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1aee4-107">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1aee4-108">類型： **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="1aee4-108">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="1aee4-109">接收專案物件樹狀目錄中專案父系之 [**IWiaItem2**](-wia-iwiaitem2.md) 介面的指標位址。</span><span class="sxs-lookup"><span data-stu-id="1aee4-109">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the parent of the item in the tree of item objects.</span></span> <span data-ttu-id="1aee4-110">如果在樹狀結構的根目錄呼叫這個方法，則傳回的位址為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1aee4-110">If this method is called on the root of the tree, then the returned address is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1aee4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1aee4-111">Return value</span></span>

<span data-ttu-id="1aee4-112">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1aee4-112">Type: **HRESULT**</span></span>

<span data-ttu-id="1aee4-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="1aee4-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1aee4-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1aee4-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1aee4-115">備註</span><span class="sxs-lookup"><span data-stu-id="1aee4-115">Remarks</span></span>

<span data-ttu-id="1aee4-116">針對 WIA 2.0 硬體裝置的物件樹狀結構中的任何 [**IWiaItem2**](-wia-iwiaitem2.md) 物件，應用程式會呼叫這個函式，以抓取父專案的指標。</span><span class="sxs-lookup"><span data-stu-id="1aee4-116">Given any [**IWiaItem2**](-wia-iwiaitem2.md) object in the object tree of a WIA 2.0 hardware device, the application retrieves a pointer to the parent item by calling this function.</span></span>

<span data-ttu-id="1aee4-117">如果這些指標不是 **Null**，則應用程式必須在其透過 *ppIWiaItem2* 參數接收的介面指標上呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法。</span><span class="sxs-lookup"><span data-stu-id="1aee4-117">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter if these pointers are not **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1aee4-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="1aee4-118">Requirements</span></span>



| <span data-ttu-id="1aee4-119">需求</span><span class="sxs-lookup"><span data-stu-id="1aee4-119">Requirement</span></span> | <span data-ttu-id="1aee4-120">值</span><span class="sxs-lookup"><span data-stu-id="1aee4-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1aee4-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1aee4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1aee4-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1aee4-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1aee4-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1aee4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1aee4-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1aee4-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1aee4-125">標頭</span><span class="sxs-lookup"><span data-stu-id="1aee4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1aee4-126"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="1aee4-126"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="1aee4-127">Idl</span><span class="sxs-lookup"><span data-stu-id="1aee4-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1aee4-128"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="1aee4-128"><dt>Wia.idl</dt></span></span> </dl> |



 

 
