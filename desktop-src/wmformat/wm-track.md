---
title: WM/曲目
description: WM/Track 屬性包含內容的曲目編號。 這個屬性是以零為基底，而且支援回溯相容性。 新內容應該改用 WM/TrackNumber 屬性。
ms.assetid: c763d7b0-9d12-4a4e-8c9f-9cf67bd2a02b
keywords:
- WM/Track windows 媒體格式
topic_type:
- apiref
api_name:
- WM/Track
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 244426175ea74bc0281f8822964c2fc0bfa37aa7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104372781"
---
# <a name="wmtrack"></a><span data-ttu-id="c37d9-106">WM/曲目</span><span class="sxs-lookup"><span data-stu-id="c37d9-106">WM/Track</span></span>

<span data-ttu-id="c37d9-107">**WM/Track** 屬性包含內容的曲目編號。</span><span class="sxs-lookup"><span data-stu-id="c37d9-107">The **WM/Track** attribute contains the track number of the content.</span></span> <span data-ttu-id="c37d9-108">這個屬性是以零為基底，而且支援回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="c37d9-108">This attribute is zero-based and is supported for backward compatibility.</span></span> <span data-ttu-id="c37d9-109">新內容應該改用 [**WM/TrackNumber**](wm-tracknumber.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="c37d9-109">New content should use the [**WM/TrackNumber**](wm-tracknumber.md) attribute instead.</span></span>

## <a name="global-constant"></a><span data-ttu-id="c37d9-110">全域常數</span><span class="sxs-lookup"><span data-stu-id="c37d9-110">Global Constant</span></span>

<span data-ttu-id="c37d9-111">g \_ wszWMTrack</span><span class="sxs-lookup"><span data-stu-id="c37d9-111">g\_wszWMTrack</span></span>

## <a name="data-type"></a><span data-ttu-id="c37d9-112">資料類型</span><span class="sxs-lookup"><span data-stu-id="c37d9-112">Data Type</span></span>

<span data-ttu-id="c37d9-113">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="c37d9-113">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="c37d9-114">備註</span><span class="sxs-lookup"><span data-stu-id="c37d9-114">Remarks</span></span>

<span data-ttu-id="c37d9-115">許多現有的應用程式都會將 **WM/Track** 的值寫入為 **DWORD**。</span><span class="sxs-lookup"><span data-stu-id="c37d9-115">Many existing applications write the value for **WM/Track** as a **DWORD**.</span></span> <span data-ttu-id="c37d9-116">如果您建立的應用程式會播放來自不明來源的檔案，您應該包含程式碼來處理字串和 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="c37d9-116">If you create an application that plays files from unknown sources, you should include code to handle both string and **DWORD** values.</span></span>

## <a name="see-also"></a><span data-ttu-id="c37d9-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c37d9-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c37d9-118">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="c37d9-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




