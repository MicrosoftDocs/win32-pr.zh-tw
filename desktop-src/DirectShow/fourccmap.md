---
description: FOURCCMap 類別提供 GUID 媒體子類型與舊樣式 FOURCC 32 位媒體標記之間的轉換。
ms.assetid: f77f1da9-34f6-44a0-9f1a-7db2e5a26268
title: FOURCCMap 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap
api_type:
- COM
api_location: ''
ms.openlocfilehash: fd30a0f04d98b4c6ba4b7716a1a72d527873dbff
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109201"
---
# <a name="fourccmap-class"></a><span data-ttu-id="4df82-103">FOURCCMap 類別</span><span class="sxs-lookup"><span data-stu-id="4df82-103">FOURCCMap class</span></span>

![fourccmap 類別階層](images/fourcc01.png)

<span data-ttu-id="4df82-105">**FOURCCMap** 類別提供 **GUID** 媒體子類型與舊樣式 **FOURCC** 32 位媒體標記之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="4df82-105">The **FOURCCMap** class provides conversion between **GUID** media subtypes and old-style **FOURCC** 32-bit media tags.</span></span> <span data-ttu-id="4df82-106">在原始的 Windows 多媒體 Api 中，媒體類型已標記為32位值（從 4 8 位字元建立），也稱為 **FOURCC** s。</span><span class="sxs-lookup"><span data-stu-id="4df82-106">In the original Windows multimedia APIs, media types were tagged with 32-bit values created from four 8-bit characters and were known as **FOURCC** s.</span></span> <span data-ttu-id="4df82-107">DirectShow 媒體類型具有子類型的 **GUID**，部分原因在於建立新 **FOURCC** 的 (建立時，必須向 Microsoft) 註冊。</span><span class="sxs-lookup"><span data-stu-id="4df82-107">DirectShow media types have **GUID** s for the subtype, partly because these are simpler to create (creation of a new **FOURCC** requires its registration with Microsoft).</span></span> <span data-ttu-id="4df82-108">由於 **FOURCC** 是唯一的，因此您可以配置代表 **FOURCC** 的 4000000000 **GUID** 範圍，藉以進行一對一的對應。</span><span class="sxs-lookup"><span data-stu-id="4df82-108">Because **FOURCC** s are unique, a one-to-one mapping has been made possible by allocating a range of 4,000 million **GUID** s representing **FOURCC** s.</span></span> <span data-ttu-id="4df82-109">此範圍是所有格式的 **GUID**：</span><span class="sxs-lookup"><span data-stu-id="4df82-109">This range is all **GUID** s of the form:</span></span>

`XXXXXXXX-0000-0010-8000-00AA00389B71`

<span data-ttu-id="4df82-110">此類別可簡化 **GUID** s 和 **FOURCC** 之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="4df82-110">This class simplifies conversion between **GUID** s and **FOURCC** s.</span></span> <span data-ttu-id="4df82-111">這僅適用于相容性。</span><span class="sxs-lookup"><span data-stu-id="4df82-111">This is for compatibility only.</span></span> <span data-ttu-id="4df82-112">建議所有新的媒體子類型都以 Guidgen.exe 或類似工具所建立的 **GUID** 來表示，而不是藉由對應 **FOURCC**。</span><span class="sxs-lookup"><span data-stu-id="4df82-112">It is recommended that all new media subtypes be represented by **GUID** s created by Guidgen.exe or a similar tool, and not by mapping **FOURCC** s.</span></span>

<span data-ttu-id="4df82-113">物件衍生自 **guid**，沒有額外的資料成員，而且可以轉換成 **guid**。</span><span class="sxs-lookup"><span data-stu-id="4df82-113">The object is derived from a **GUID**, with no extra data members, and can be cast to a **GUID**.</span></span> <span data-ttu-id="4df82-114">物件可以在結構時間傳遞 **FOURCC** 。</span><span class="sxs-lookup"><span data-stu-id="4df82-114">The object can be passed a **FOURCC** at construction time.</span></span> <span data-ttu-id="4df82-115">預設的函式會將 **FOURCC** 初始化為零。</span><span class="sxs-lookup"><span data-stu-id="4df82-115">The default constructor will initialize the **FOURCC** to zero.</span></span>

<span data-ttu-id="4df82-116">[**GetFOURCC**](fourccmap-getfourcc.md)和 [**SetFOURCC**](fourccmap-setfourcc.md)方法不會檢查 **GUID** 的固定部分是否對應到 **FOURCC** 範圍。</span><span class="sxs-lookup"><span data-stu-id="4df82-116">The [**GetFOURCC**](fourccmap-getfourcc.md) and [**SetFOURCC**](fourccmap-setfourcc.md) methods do not check that the fixed portions of the **GUID** correspond to the **FOURCC** range.</span></span> <span data-ttu-id="4df82-117">因此，如果您將 **guid** 的指標轉換成 **FOURCC** 的指標，然後設定或取得 **FOURCC** 欄位，您也需要另外檢查 **guid** 是否在 **FOURCC** 範圍內。</span><span class="sxs-lookup"><span data-stu-id="4df82-117">Thus, if you cast a pointer to a **GUID** into a pointer to a **FOURCC** and then set or get the **FOURCC** field, you also need to check separately that the **GUID** is within the **FOURCC** range.</span></span>

## <a name="member-functions"></a><span data-ttu-id="4df82-118">成員函數</span><span class="sxs-lookup"><span data-stu-id="4df82-118">Member Functions</span></span>



|                                          |                                                          |
|------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="4df82-119">**FOURCCMap**</span><span class="sxs-lookup"><span data-stu-id="4df82-119">**FOURCCMap**</span></span>](fourccmap-fourccmap.md) | <span data-ttu-id="4df82-120">函式方法。</span><span class="sxs-lookup"><span data-stu-id="4df82-120">Constructor method.</span></span>                                      |
| [<span data-ttu-id="4df82-121">**GetFOURCC**</span><span class="sxs-lookup"><span data-stu-id="4df82-121">**GetFOURCC**</span></span>](fourccmap-getfourcc.md) | <span data-ttu-id="4df82-122">從 **FOURCCMap** 物件中抓取 **FOURCC** 。</span><span class="sxs-lookup"><span data-stu-id="4df82-122">Retrieves the **FOURCC** from a **FOURCCMap** object.</span></span>    |
| [<span data-ttu-id="4df82-123">**SetFOURCC**</span><span class="sxs-lookup"><span data-stu-id="4df82-123">**SetFOURCC**</span></span>](fourccmap-setfourcc.md) | <span data-ttu-id="4df82-124">設定 **FOURCCMap** 物件的 **FOURCC** 部分。</span><span class="sxs-lookup"><span data-stu-id="4df82-124">Sets the **FOURCC** portion of the **FOURCCMap** object.</span></span> |



 

 

 



