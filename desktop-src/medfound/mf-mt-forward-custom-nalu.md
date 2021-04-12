---
description: 指定 (NAL) 單位類型的網路抽象層應該在輸出範例上由解碼器轉送。
ms.assetid: 2A1D8629-EB66-4F72-9AD7-93123D941BB0
title: 'MF_MT_FORWARD_CUSTOM_NALU 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93a318523f52ab7d65450c4c2f35b7bfbf63d5f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513960"
---
# <a name="mf_mt_forward_custom_nalu-attribute"></a><span data-ttu-id="dcb52-103">MF \_ MT \_ 向前 \_ 自訂 \_ NALU 屬性</span><span class="sxs-lookup"><span data-stu-id="dcb52-103">MF\_MT\_FORWARD\_CUSTOM\_NALU attribute</span></span>

<span data-ttu-id="dcb52-104">指定 (NAL) 單位類型的網路抽象層應該在輸出範例上由解碼器轉送。</span><span class="sxs-lookup"><span data-stu-id="dcb52-104">Specifies that network abstraction layer (NAL) unit types should be forwarded on output samples by the decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="dcb52-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="dcb52-105">Data type</span></span>

<span data-ttu-id="dcb52-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="dcb52-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="dcb52-107">備註</span><span class="sxs-lookup"><span data-stu-id="dcb52-107">Remarks</span></span>

<span data-ttu-id="dcb52-108">如果解碼器剖析 NALU，則不會轉送。</span><span class="sxs-lookup"><span data-stu-id="dcb52-108">If the decoder parses a NALU then it will not be forwarded.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcb52-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="dcb52-109">Requirements</span></span>



| <span data-ttu-id="dcb52-110">需求</span><span class="sxs-lookup"><span data-stu-id="dcb52-110">Requirement</span></span> | <span data-ttu-id="dcb52-111">值</span><span class="sxs-lookup"><span data-stu-id="dcb52-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dcb52-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dcb52-112">Minimum supported client</span></span><br/> | <span data-ttu-id="dcb52-113">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dcb52-113">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="dcb52-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dcb52-114">Minimum supported server</span></span><br/> | <span data-ttu-id="dcb52-115">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dcb52-115">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="dcb52-116">標頭</span><span class="sxs-lookup"><span data-stu-id="dcb52-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcb52-117"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="dcb52-117"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




