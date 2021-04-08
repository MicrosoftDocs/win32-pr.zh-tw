---
title: VBRPeak
description: VBRPeak 屬性包含變數位元速率的最高暫時位速率 (VBR) 編碼的資料流程。
ms.assetid: 7b735145-8235-4efb-986f-952989b739bc
keywords:
- VBRPeak windows Media 格式
topic_type:
- apiref
api_name:
- VBRPeak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e8aacb076c3e92cfa676e73e945506cc4942bf4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022566"
---
# <a name="vbrpeak"></a><span data-ttu-id="52c07-104">VBRPeak</span><span class="sxs-lookup"><span data-stu-id="52c07-104">VBRPeak</span></span>

<span data-ttu-id="52c07-105">**VBRPeak** 屬性包含變數位元速率的最高暫時位速率 (VBR) 編碼的資料流程。</span><span class="sxs-lookup"><span data-stu-id="52c07-105">The **VBRPeak** attribute contains the highest momentary bit rate in a variable bit rate (VBR) encoded stream.</span></span>

## <a name="global-constant"></a><span data-ttu-id="52c07-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="52c07-106">Global Constant</span></span>

<span data-ttu-id="52c07-107">g \_ wszVBRPeak</span><span class="sxs-lookup"><span data-stu-id="52c07-107">g\_wszVBRPeak</span></span>

## <a name="data-type"></a><span data-ttu-id="52c07-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="52c07-108">Data Type</span></span>

<span data-ttu-id="52c07-109">**WMT \_ 類型 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="52c07-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="52c07-110">備註</span><span class="sxs-lookup"><span data-stu-id="52c07-110">Remarks</span></span>

<span data-ttu-id="52c07-111">存取寫入器物件的 **IWMHeaderInfo3** 介面時，您可以加入或變更此值。</span><span class="sxs-lookup"><span data-stu-id="52c07-111">When accessing the **IWMHeaderInfo3** interface of the writer object, you can add or change this value.</span></span> <span data-ttu-id="52c07-112">在其他物件 (中繼資料編輯器、讀取器和同步讀取器) ，此值是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="52c07-112">In other objects (metadata editor, reader, and synchronous reader), this value is read-only.</span></span>

<span data-ttu-id="52c07-113">寫入器會自動為每個 VBR 串流寫入 **VBRPeak** 值。</span><span class="sxs-lookup"><span data-stu-id="52c07-113">The writer automatically writes a **VBRPeak** value for each VBR stream.</span></span>

## <a name="see-also"></a><span data-ttu-id="52c07-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="52c07-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52c07-115">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="52c07-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




