---
description: 指定編碼資料流程的最大緩衝區視窗（以毫秒為單位）。
ms.assetid: d4cb80fe-cf44-4260-a132-9d264c3efb22
title: 'MFPKEY_STAT_BMAX 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0941d92cb6e71b3eabaaae5cad14aa080cdaeffc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980160"
---
# <a name="mfpkey_stat_bmax-property"></a><span data-ttu-id="cd314-103">MFPKEY \_ STAT \_ BMAX 屬性</span><span class="sxs-lookup"><span data-stu-id="cd314-103">MFPKEY\_STAT\_BMAX Property</span></span>

<span data-ttu-id="cd314-104">指定編碼資料流程的最大緩衝區視窗（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="cd314-104">Specifies the maximum buffer window, in milliseconds, of an encoded stream.</span></span> <span data-ttu-id="cd314-105">唯讀。</span><span class="sxs-lookup"><span data-stu-id="cd314-105">Read-only.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="cd314-106">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="cd314-106">Constant for IPropertyBag</span></span>

<span data-ttu-id="cd314-107">**g \_ wszWMVCMaxBitrate**</span><span class="sxs-lookup"><span data-stu-id="cd314-107">**g\_wszWMVCMaxBitrate**</span></span>

## <a name="data-type"></a><span data-ttu-id="cd314-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="cd314-108">Data Type</span></span>

<span data-ttu-id="cd314-109">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="cd314-109">**VT\_I4**</span></span>

## <a name="remarks"></a><span data-ttu-id="cd314-110">備註</span><span class="sxs-lookup"><span data-stu-id="cd314-110">Remarks</span></span>

<span data-ttu-id="cd314-111">若要判斷已編碼資料流程的緩衝區視窗上限，請在編碼結束時讀取這個屬性。</span><span class="sxs-lookup"><span data-stu-id="cd314-111">To determine the maximum buffer windows of an encoded stream, read this property at the end of encoding.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd314-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd314-112">Requirements</span></span>



| <span data-ttu-id="cd314-113">需求</span><span class="sxs-lookup"><span data-stu-id="cd314-113">Requirement</span></span> | <span data-ttu-id="cd314-114">值</span><span class="sxs-lookup"><span data-stu-id="cd314-114">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd314-115">用戶端</span><span class="sxs-lookup"><span data-stu-id="cd314-115">Client</span></span><br/> | <span data-ttu-id="cd314-116">Windows XP、Windows Vista 或 Windows 7</span><span class="sxs-lookup"><span data-stu-id="cd314-116">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="cd314-117">標頭</span><span class="sxs-lookup"><span data-stu-id="cd314-117">Header</span></span><br/> | <dl> <span data-ttu-id="cd314-118"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="cd314-118"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd314-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cd314-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd314-120">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="cd314-120">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




