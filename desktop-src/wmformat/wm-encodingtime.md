---
title: WM/EncodingTime
description: WM/EncodingTime 屬性包含內容編碼時間的時間戳記。
ms.assetid: 63da9392-264d-40bb-99fd-56db93801941
keywords:
- WM/EncodingTime windows Media 格式
topic_type:
- apiref
api_name:
- WM/EncodingTime
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d27119a9b54e3de22fe620f556c672bd4fe1a17
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022663"
---
# <a name="wmencodingtime"></a><span data-ttu-id="e9f5a-104">WM/EncodingTime</span><span class="sxs-lookup"><span data-stu-id="e9f5a-104">WM/EncodingTime</span></span>

<span data-ttu-id="e9f5a-105">**WM/EncodingTime** 屬性包含內容編碼時間的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="e9f5a-105">The **WM/EncodingTime** attribute contains a time stamp of the time at which the content was encoded.</span></span>

## <a name="global-constant"></a><span data-ttu-id="e9f5a-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="e9f5a-106">Global Constant</span></span>

<span data-ttu-id="e9f5a-107">g \_ wszWMEncodingTime</span><span class="sxs-lookup"><span data-stu-id="e9f5a-107">g\_wszWMEncodingTime</span></span>

## <a name="data-type"></a><span data-ttu-id="e9f5a-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="e9f5a-108">Data Type</span></span>

<span data-ttu-id="e9f5a-109">**FILETIME** (**WMT \_ 類型 \_ QWORD**) </span><span class="sxs-lookup"><span data-stu-id="e9f5a-109">**FILETIME** (**WMT\_TYPE\_QWORD**)</span></span>

## <a name="remarks"></a><span data-ttu-id="e9f5a-110">備註</span><span class="sxs-lookup"><span data-stu-id="e9f5a-110">Remarks</span></span>

<span data-ttu-id="e9f5a-111">這個屬性會使用 FILETIME 值，這是代表自1601年1月1日以來經過的 100-納秒時間單位數的64位值。</span><span class="sxs-lookup"><span data-stu-id="e9f5a-111">This attribute uses a FILETIME value, which is a 64-bit value representing the number of 100-nanosecond time units elapsed since January 1, 1601.</span></span> <span data-ttu-id="e9f5a-112">如需 FILETIME 的詳細資訊，請參閱 Platform SDK 的 Windows 系統資訊一節。</span><span class="sxs-lookup"><span data-stu-id="e9f5a-112">For more information about the FILETIME, see the Windows System Information section of the Platform SDK.</span></span>

<span data-ttu-id="e9f5a-113">這不是編碼屬性。</span><span class="sxs-lookup"><span data-stu-id="e9f5a-113">This is not a coded attribute.</span></span> <span data-ttu-id="e9f5a-114">如果您想要將它包含在您的檔案中，則必須手動設定它。</span><span class="sxs-lookup"><span data-stu-id="e9f5a-114">You must set it manually if you want to include it in your files.</span></span>

## <a name="see-also"></a><span data-ttu-id="e9f5a-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9f5a-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9f5a-116">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="e9f5a-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




