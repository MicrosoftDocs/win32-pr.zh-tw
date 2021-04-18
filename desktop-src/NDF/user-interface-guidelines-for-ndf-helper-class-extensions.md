---
title: NDF helper 類別延伸的 UI 指導方針
description: 建立協助程式類別時，您將需要建立文字，以協助使用者瞭解事件的原因，以及可採取的可能修復步驟。
ms.assetid: f13f3621-ab82-4e22-9442-0a4d57c368fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e48357ba6561ab135e2c341409c22d1edf3fb7d
ms.sourcegitcommit: 2e9db3c7d9a3dbea15196b03c883846fad6f32be
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/12/2019
ms.locfileid: "104313586"
---
# <a name="ui-guidelines-for-ndf-helper-class-extensions"></a><span data-ttu-id="ac9d6-103">NDF helper 類別延伸的 UI 指導方針</span><span class="sxs-lookup"><span data-stu-id="ac9d6-103">UI guidelines for NDF helper class extensions</span></span>

<span data-ttu-id="ac9d6-104">建立協助程式類別時，您將需要建立文字，以協助使用者瞭解事件的原因，以及可採取的可能修復步驟。</span><span class="sxs-lookup"><span data-stu-id="ac9d6-104">When building your helper class, you will need to create text to help the user understand the cause of an incident and the possible repair steps which can be taken.</span></span>

## <a name="root-cause-and-repair"></a><span data-ttu-id="ac9d6-105">根本原因和修復</span><span class="sxs-lookup"><span data-stu-id="ac9d6-105">Root Cause and Repair</span></span>

<span data-ttu-id="ac9d6-106">發生事件時，會出現一個對話方塊，告知使用者發生了什麼事。</span><span class="sxs-lookup"><span data-stu-id="ac9d6-106">When an incident occurs, a dialog box will appear to inform the user about what has happened.</span></span> <span data-ttu-id="ac9d6-107">您所建立的文字將會出現在兩個不同的區域中。</span><span class="sxs-lookup"><span data-stu-id="ac9d6-107">The text that you create will appear in two separate areas.</span></span>

-   <span data-ttu-id="ac9d6-108">**根本原因**：問題原因的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="ac9d6-108">**Root Cause**: A brief description of the cause of the issue.</span></span> <span data-ttu-id="ac9d6-109">包含可協助系統管理員或 advanced 使用者針對問題進行疑難排解的資訊。</span><span class="sxs-lookup"><span data-stu-id="ac9d6-109">Contains information to help an administrator or advanced user troubleshoot the problem.</span></span>
-   <span data-ttu-id="ac9d6-110">**修復**：展開根本原因，以提供使用者可採取之步驟的詳細資料，而不會變得太長。</span><span class="sxs-lookup"><span data-stu-id="ac9d6-110">**Repair**: Expands on the root cause to provide more details about the steps that a user can take, without getting too lengthy.</span></span>

<span data-ttu-id="ac9d6-111">每個根本原因或修復都應該有標題和描述。</span><span class="sxs-lookup"><span data-stu-id="ac9d6-111">Each root cause or repair should have a title and a description.</span></span> <span data-ttu-id="ac9d6-112">第一個 "n" 字元之前的所有文字 \\ 將會用於標題。</span><span class="sxs-lookup"><span data-stu-id="ac9d6-112">All text before the first "\\n" character will be used for the title.</span></span> <span data-ttu-id="ac9d6-113">前 "n" 個字元後面的所有文字 \\ (包括任何後續分行符號) 將用於描述。</span><span class="sxs-lookup"><span data-stu-id="ac9d6-113">All text following the first "\\n" character (including any subsequent line breaks) will be used for the description.</span></span>

## <a name="title-guidelines"></a><span data-ttu-id="ac9d6-114">標題指導方針</span><span class="sxs-lookup"><span data-stu-id="ac9d6-114">Title Guidelines</span></span>

<span data-ttu-id="ac9d6-115">根本原因或修復的標題應該遵循下列指導方針：</span><span class="sxs-lookup"><span data-stu-id="ac9d6-115">The title of a root cause or repair should follow these guidelines:</span></span>

-   <span data-ttu-id="ac9d6-116">必須為128個字元或更少。</span><span class="sxs-lookup"><span data-stu-id="ac9d6-116">Must be 128 characters or fewer.</span></span> <span data-ttu-id="ac9d6-117">建議 (40 個字元或更少。 ) </span><span class="sxs-lookup"><span data-stu-id="ac9d6-117">(40 characters or less is recommended.)</span></span>
-   <span data-ttu-id="ac9d6-118">不應以句號結尾。</span><span class="sxs-lookup"><span data-stu-id="ac9d6-118">Should not end with a period.</span></span>

## <a name="description-guidelines"></a><span data-ttu-id="ac9d6-119">描述方針</span><span class="sxs-lookup"><span data-stu-id="ac9d6-119">Description Guidelines</span></span>

<span data-ttu-id="ac9d6-120">根本原因或修復的描述應遵循下列指導方針：</span><span class="sxs-lookup"><span data-stu-id="ac9d6-120">The description of a root cause or repair should follow these guidelines:</span></span>

-   <span data-ttu-id="ac9d6-121">必須為512個字元或更少。</span><span class="sxs-lookup"><span data-stu-id="ac9d6-121">Must be 512 characters or fewer.</span></span>
-   <span data-ttu-id="ac9d6-122">每個句子的結尾都應該是句號。</span><span class="sxs-lookup"><span data-stu-id="ac9d6-122">Each sentence should end with a period.</span></span>
-   <span data-ttu-id="ac9d6-123">" \\ N" 字元可以用來在描述中建立分行符號。</span><span class="sxs-lookup"><span data-stu-id="ac9d6-123">The "\\n" character may be used to create a line break in the description.</span></span>

 

 




