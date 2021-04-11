---
description: 如果 ICE90 發現快捷方式的目錄已指定為公用屬性，則會張貼警告。
ms.assetid: 47565d9b-c3c2-4a5c-8f91-2b3912a63b47
title: ICE90
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b4063d06aa5a0a8688e2a411040d4b64f58f75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848844"
---
# <a name="ice90"></a><span data-ttu-id="27b91-103">ICE90</span><span class="sxs-lookup"><span data-stu-id="27b91-103">ICE90</span></span>

<span data-ttu-id="27b91-104">如果 ICE90 發現快捷方式的目錄已指定為公用屬性，則會張貼警告。</span><span class="sxs-lookup"><span data-stu-id="27b91-104">ICE90 posts a warning if it finds that a shortcut's directory has been specified as a public property.</span></span> <span data-ttu-id="27b91-105">[公用屬性](public-properties.md)的名稱是以大寫字母撰寫。</span><span class="sxs-lookup"><span data-stu-id="27b91-105">The names of [Public Properties](public-properties.md) are written in uppercase letters.</span></span> <span data-ttu-id="27b91-106">如果 [**ALLUSERS**](allusers.md) 屬性的值變更，則公用屬性指定的快捷方式可能無法運作。</span><span class="sxs-lookup"><span data-stu-id="27b91-106">A shortcut specified by a public property may not work if the value of the [**ALLUSERS**](allusers.md) property changes.</span></span>

<span data-ttu-id="27b91-107">此 ICE 自訂動作會驗證快速鍵資料表並使用目錄資料表。</span><span class="sxs-lookup"><span data-stu-id="27b91-107">This ICE custom action validates the Shortcut table and uses the Directory table.</span></span> <span data-ttu-id="27b91-108">如果目錄資料表不存在，則會在未驗證快速鍵資料表的情況下傳回，而且不會張貼任何錯誤或警告。</span><span class="sxs-lookup"><span data-stu-id="27b91-108">If the Directory table is not present, it returns without validating the Shortcut table and posts no errors or warnings.</span></span>

## <a name="result"></a><span data-ttu-id="27b91-109">結果</span><span class="sxs-lookup"><span data-stu-id="27b91-109">Result</span></span>

<span data-ttu-id="27b91-110">ICE90 會張貼下列警告。</span><span class="sxs-lookup"><span data-stu-id="27b91-110">ICE90 posts the following warning.</span></span>



| <span data-ttu-id="27b91-111">ICE90 錯誤</span><span class="sxs-lookup"><span data-stu-id="27b91-111">ICE90 error</span></span>                                                                                                                                                                                                                    | <span data-ttu-id="27b91-112">Description</span><span class="sxs-lookup"><span data-stu-id="27b91-112">Description</span></span>                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="27b91-113">快速鍵 ' \[ 1 \] ' 的目錄是公用屬性 (所有 CAPS) ，而且位於使用者設定檔目錄下。</span><span class="sxs-lookup"><span data-stu-id="27b91-113">The shortcut '\[1\]' has a directory that is a public property (ALL CAPS) and is under user profile directory.</span></span> <span data-ttu-id="27b91-114">如果 UI 順序中的 [**ALLUSERS**](allusers.md) 屬性值變更，這會導致問題。</span><span class="sxs-lookup"><span data-stu-id="27b91-114">This results in a problem if the value of the [**ALLUSERS**](allusers.md) property changes in the UI sequence.</span></span> | <span data-ttu-id="27b91-115">快速鍵的目錄已指定為公用屬性。</span><span class="sxs-lookup"><span data-stu-id="27b91-115">A shortcut's directory has been specified as a public property.</span></span> |



 

## <a name="example"></a><span data-ttu-id="27b91-116">範例</span><span class="sxs-lookup"><span data-stu-id="27b91-116">Example</span></span>

<span data-ttu-id="27b91-117">ICE90 會報告下列範例警告：</span><span class="sxs-lookup"><span data-stu-id="27b91-117">ICE90 reports the following warning for the example:</span></span>

``` syntax
The shortcut 'Shortcut1' has a directory that is a public property (ALL CAPS) 
and is under user profile directory. This results in a problem if the value 
of the ALLUSERS property changes in the UI sequence.
```

<span data-ttu-id="27b91-118">在此範例中，MYDIR 是在使用者設定檔下。</span><span class="sxs-lookup"><span data-stu-id="27b91-118">In this example, MYDIR is under a users profile.</span></span> <span data-ttu-id="27b91-119">ICE90 會張貼警告，因為目標目錄的位置是由公用屬性 MYDIR 所指定。</span><span class="sxs-lookup"><span data-stu-id="27b91-119">ICE90 posts a warning because the location of the target directory is specified by a public property, MYDIR.</span></span> <span data-ttu-id="27b91-120">使用者可變更 MYDIR 或 [**ALLUSERS**](allusers.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="27b91-120">A user may change MYDIR or [**ALLUSERS**](allusers.md) property.</span></span> <span data-ttu-id="27b91-121">如果針對每部電腦 [安裝內容](installation-context.md)設定 **ALLUSERS** ，而 MYDIR 是在使用者設定檔下，MYDIR 中的快捷方式檔案就會複製到 [所有使用者] 設定檔下，而不是特定使用者的設定檔。</span><span class="sxs-lookup"><span data-stu-id="27b91-121">If **ALLUSERS** is set for the per-machine [installation context](installation-context.md), and MYDIR is under a users profile, the shortcut file in MYDIR are copied under the "All Users" profile and not a particular user's profile.</span></span> <span data-ttu-id="27b91-122">如果針對每個使用者安裝內容設定 **ALLUSERS** ，MYDIR 中的快捷方式檔案就會複製到特定使用者的設定檔中，而不會提供給其他使用者使用。</span><span class="sxs-lookup"><span data-stu-id="27b91-122">If **ALLUSERS** is set for the per-user installation context, the shortcut file in MYDIR is copied into a particular user's profile and is not available to other users.</span></span>

<span data-ttu-id="27b91-123"> (部分) 的[快捷方式資料表](shortcut-table.md)</span><span class="sxs-lookup"><span data-stu-id="27b91-123">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="27b91-124">快速鍵</span><span class="sxs-lookup"><span data-stu-id="27b91-124">Shortcut</span></span>  | <span data-ttu-id="27b91-125">目錄\_</span><span class="sxs-lookup"><span data-stu-id="27b91-125">Directory\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="27b91-126">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="27b91-126">Shortcut1</span></span> | <span data-ttu-id="27b91-127">MYDIR</span><span class="sxs-lookup"><span data-stu-id="27b91-127">MYDIR</span></span>       |



 

<span data-ttu-id="27b91-128">[目錄資料表](directory-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="27b91-128">[Directory Table](directory-table.md) (partial)</span></span>



| <span data-ttu-id="27b91-129">目錄</span><span class="sxs-lookup"><span data-stu-id="27b91-129">Directory</span></span> | <span data-ttu-id="27b91-130">目錄 \_ 父系</span><span class="sxs-lookup"><span data-stu-id="27b91-130">Directory\_Parent</span></span> |
|-----------|-------------------|
| <span data-ttu-id="27b91-131">MYDIR</span><span class="sxs-lookup"><span data-stu-id="27b91-131">MYDIR</span></span>     | <span data-ttu-id="27b91-132">ProgramMenuFolder</span><span class="sxs-lookup"><span data-stu-id="27b91-132">ProgramMenuFolder</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="27b91-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="27b91-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27b91-134">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="27b91-134">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



