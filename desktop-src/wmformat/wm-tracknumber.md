---
title: WM/TrackNumber
description: WM/TrackNumber 屬性包含內容的曲目編號。 這個屬性是以1為基礎。
ms.assetid: cd338cd9-a5de-4311-8089-1d5d90570f69
keywords:
- WM/TrackNumber windows Media 格式
topic_type:
- apiref
api_name:
- WM/TrackNumber
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d55691335faaf835b270013c6499197c0e3f7bee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106999789"
---
# <a name="wmtracknumber"></a><span data-ttu-id="09413-105">WM/TrackNumber</span><span class="sxs-lookup"><span data-stu-id="09413-105">WM/TrackNumber</span></span>

<span data-ttu-id="09413-106">**WM/TrackNumber** 屬性包含內容的曲目編號。</span><span class="sxs-lookup"><span data-stu-id="09413-106">The **WM/TrackNumber** attribute contains the track number of the content.</span></span> <span data-ttu-id="09413-107">這個屬性是以1為基礎。</span><span class="sxs-lookup"><span data-stu-id="09413-107">This attribute is 1-based.</span></span>

## <a name="global-constant"></a><span data-ttu-id="09413-108">全域常數</span><span class="sxs-lookup"><span data-stu-id="09413-108">Global Constant</span></span>

<span data-ttu-id="09413-109">g \_ wszWMTrackNumber</span><span class="sxs-lookup"><span data-stu-id="09413-109">g\_wszWMTrackNumber</span></span>

## <a name="data-type"></a><span data-ttu-id="09413-110">資料類型</span><span class="sxs-lookup"><span data-stu-id="09413-110">Data Type</span></span>

<span data-ttu-id="09413-111">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="09413-111">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="09413-112">備註</span><span class="sxs-lookup"><span data-stu-id="09413-112">Remarks</span></span>

<span data-ttu-id="09413-113">許多現有的應用程式都會將 **WM/TrackNumber** 的值寫入為 **DWORD**。</span><span class="sxs-lookup"><span data-stu-id="09413-113">Many existing applications write the value for **WM/TrackNumber** as a **DWORD**.</span></span> <span data-ttu-id="09413-114">如果您建立的應用程式會播放來自不明來源的檔案，您應該包含程式碼來處理字串和 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="09413-114">If you create an application that plays files from unknown sources, you should include code to handle both string and **DWORD** values.</span></span>

## <a name="see-also"></a><span data-ttu-id="09413-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="09413-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09413-116">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="09413-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




