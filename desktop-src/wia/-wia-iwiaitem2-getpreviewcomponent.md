---
description: 取得 (WIA) 2.0 preview 元件的 Windows 映像取得。
ms.assetid: 0b773c4c-f080-41fa-8902-4243a80fc67c
title: 'IWiaItem2：： GetPreviewComponent 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetPreviewComponent
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2e0881f68044c30731322c89d6cc2f19ce7277a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113305"
---
# <a name="iwiaitem2getpreviewcomponent-method"></a><span data-ttu-id="152fb-103">IWiaItem2：： GetPreviewComponent 方法</span><span class="sxs-lookup"><span data-stu-id="152fb-103">IWiaItem2::GetPreviewComponent method</span></span>

<span data-ttu-id="152fb-104">取得 (WIA) 2.0 preview 元件的 Windows 映像取得。</span><span class="sxs-lookup"><span data-stu-id="152fb-104">Gets the Windows Image Acquisition (WIA) 2.0 preview component.</span></span>

## <a name="syntax"></a><span data-ttu-id="152fb-105">語法</span><span class="sxs-lookup"><span data-stu-id="152fb-105">Syntax</span></span>


```C++
HRESULT GetPreviewComponent(
  [in]  LONG        lFlags,
  [out] IWiaPreview **ppWiaPreview
);
```



## <a name="parameters"></a><span data-ttu-id="152fb-106">參數</span><span class="sxs-lookup"><span data-stu-id="152fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="152fb-107">*lFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="152fb-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="152fb-108">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="152fb-108">Type: **LONG**</span></span>

<span data-ttu-id="152fb-109">未使用。</span><span class="sxs-lookup"><span data-stu-id="152fb-109">Not used.</span></span> <span data-ttu-id="152fb-110">設定為0。</span><span class="sxs-lookup"><span data-stu-id="152fb-110">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="152fb-111">*ppWiaPreview* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="152fb-111">*ppWiaPreview* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="152fb-112">類型： **[ **IWiaPreview**](-wia-iwiapreview.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="152fb-112">Type: **[**IWiaPreview**](-wia-iwiapreview.md)\*\***</span></span>

<span data-ttu-id="152fb-113">傳回預覽元件之 [**IWiaPreview**](-wia-iwiapreview.md) 介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="152fb-113">Returns the address of a pointer to the [**IWiaPreview**](-wia-iwiapreview.md) interface of the preview component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="152fb-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="152fb-114">Return value</span></span>

<span data-ttu-id="152fb-115">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="152fb-115">Type: **HRESULT**</span></span>

<span data-ttu-id="152fb-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="152fb-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="152fb-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="152fb-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="152fb-118">備註</span><span class="sxs-lookup"><span data-stu-id="152fb-118">Remarks</span></span>

<span data-ttu-id="152fb-119">使用此函式可針對 WIA 2.0 硬體裝置之物件樹狀結構中的任何 [**IWiaItem2**](-wia-iwiaitem2.md) 物件，將指標傳回至 wia 2.0 preview 元件的位址。</span><span class="sxs-lookup"><span data-stu-id="152fb-119">Use this function to return a pointer to the address of the WIA 2.0 preview component for any [**IWiaItem2**](-wia-iwiaitem2.md) object in the object tree of a WIA 2.0 hardware device.</span></span>

<span data-ttu-id="152fb-120">應用程式必須在透過 *ppWiaPreview* 參數接收的介面指標上呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法。</span><span class="sxs-lookup"><span data-stu-id="152fb-120">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers that they receive through the *ppWiaPreview* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="152fb-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="152fb-121">Requirements</span></span>



| <span data-ttu-id="152fb-122">需求</span><span class="sxs-lookup"><span data-stu-id="152fb-122">Requirement</span></span> | <span data-ttu-id="152fb-123">值</span><span class="sxs-lookup"><span data-stu-id="152fb-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="152fb-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="152fb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="152fb-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="152fb-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="152fb-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="152fb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="152fb-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="152fb-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="152fb-128">標頭</span><span class="sxs-lookup"><span data-stu-id="152fb-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="152fb-129"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="152fb-129"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="152fb-130">Idl</span><span class="sxs-lookup"><span data-stu-id="152fb-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="152fb-131"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="152fb-131"><dt>Wia.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="152fb-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="152fb-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="152fb-133">**IWiaItem2**</span><span class="sxs-lookup"><span data-stu-id="152fb-133">**IWiaItem2**</span></span>](-wia-iwiaitem2.md)
</dt> <dt>

[<span data-ttu-id="152fb-134">**IWiaPreview**</span><span class="sxs-lookup"><span data-stu-id="152fb-134">**IWiaPreview**</span></span>](-wia-iwiapreview.md)
</dt> </dl>

 

 
