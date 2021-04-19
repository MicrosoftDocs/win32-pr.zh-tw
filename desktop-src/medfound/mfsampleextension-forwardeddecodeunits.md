---
description: 取得型別為 IMFCollection 的物件，其中包含 IMFSample 物件，其中包含網路抽象層單位 (NALUs) 和增補增強資訊 (SEI 由解碼器轉送的) 單位。
ms.assetid: F9FD7959-A78A-4C72-8326-EE8FF9066E6C
title: 'MFSampleExtension_ForwardedDecodeUnits 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2ab5c10a4a7fb4dfd201f9c494c1bc65e14c162
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971732"
---
# <a name="mfsampleextension_forwardeddecodeunits-attribute"></a><span data-ttu-id="a5c38-103">MFSampleExtension \_ ForwardedDecodeUnits 屬性</span><span class="sxs-lookup"><span data-stu-id="a5c38-103">MFSampleExtension\_ForwardedDecodeUnits attribute</span></span>

<span data-ttu-id="a5c38-104">取得型別為 [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) 的物件，其中包含 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 物件，其中包含網路抽象層單位 (NALUs) 和增補增強資訊 (SEI 由解碼器轉送的) 單位。</span><span class="sxs-lookup"><span data-stu-id="a5c38-104">Gets an object of type [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) containing [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) objects which contain network abstraction layer units (NALUs) and Supplemental Enhancement Information (SEI) units forwarded by a decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="a5c38-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="a5c38-105">Data type</span></span>

<span data-ttu-id="a5c38-106">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="a5c38-106">**IUnknown**</span></span>

## <a name="remarks"></a><span data-ttu-id="a5c38-107">備註</span><span class="sxs-lookup"><span data-stu-id="a5c38-107">Remarks</span></span>

<span data-ttu-id="a5c38-108">集合包含自先前畫面格起，已移除模擬防止位元組的所有自訂 NALU/SEI 單位。</span><span class="sxs-lookup"><span data-stu-id="a5c38-108">The collection contains all custom NALU/SEI units since previous frame with emulation prevention bytes removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5c38-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5c38-109">Requirements</span></span>



| <span data-ttu-id="a5c38-110">需求</span><span class="sxs-lookup"><span data-stu-id="a5c38-110">Requirement</span></span> | <span data-ttu-id="a5c38-111">值</span><span class="sxs-lookup"><span data-stu-id="a5c38-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a5c38-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a5c38-112">Minimum supported client</span></span><br/> | <span data-ttu-id="a5c38-113">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5c38-113">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a5c38-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a5c38-114">Minimum supported server</span></span><br/> | <span data-ttu-id="a5c38-115">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5c38-115">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a5c38-116">標頭</span><span class="sxs-lookup"><span data-stu-id="a5c38-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5c38-117"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="a5c38-117"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




