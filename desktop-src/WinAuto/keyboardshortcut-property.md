---
title: KeyboardShortcut 屬性
description: KeyboardShortcut 屬性描述會啟用指定之可存取物件的按鍵或按鍵組合。
ms.assetid: 42587468-f069-4ef1-868e-ac6a285e1715
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002c925151f3f1acc136190d7807d7bc814d30b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183532"
---
# <a name="keyboardshortcut-property"></a><span data-ttu-id="2a9fa-103">KeyboardShortcut 屬性</span><span class="sxs-lookup"><span data-stu-id="2a9fa-103">KeyboardShortcut Property</span></span>

<span data-ttu-id="2a9fa-104">**KeyboardShortcut** 屬性描述會啟用指定之可存取物件的按鍵或按鍵組合。</span><span class="sxs-lookup"><span data-stu-id="2a9fa-104">The **KeyboardShortcut** property describes a key or key combination that activates a specified accessible object.</span></span>

<span data-ttu-id="2a9fa-105">藉由呼叫 [**IAccessible：： get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut)，即可取出 **KeyboardShortcut** 屬性。</span><span class="sxs-lookup"><span data-stu-id="2a9fa-105">The **KeyboardShortcut** property is retrieved by calling [**IAccessible::get\_accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut).</span></span>

<span data-ttu-id="2a9fa-106">取出的字串會描述快速鍵 (也稱為 *鍵盤\*\*快捷方式*) 或 *存取金鑰* (也稱為 *助記* 鍵) 。</span><span class="sxs-lookup"><span data-stu-id="2a9fa-106">The retrieved string describes a *shortcut key* (also called a *keyboard accelerator*) or an *access key* (also called a *mnemonic*).</span></span> <span data-ttu-id="2a9fa-107">存取金鑰是功能表、功能表項目或控制項標籤（例如按下按鈕）文字中的加底線字元。</span><span class="sxs-lookup"><span data-stu-id="2a9fa-107">An access key is an underlined character in the text of a menu, menu item, or label of a control such as a push button.</span></span>

<span data-ttu-id="2a9fa-108">抓取的字串必須包含索引鍵的名稱，以及輔助按鍵或索引鍵。</span><span class="sxs-lookup"><span data-stu-id="2a9fa-108">The retrieved string must contain the name of the key along with the modifier key or keys.</span></span> <span data-ttu-id="2a9fa-109">字串必須採用下列格式，用戶端才能輕鬆地剖析它： \[ \[ 輔助按鍵 ... 索引 \] + \[ \] + \] 鍵名稱。</span><span class="sxs-lookup"><span data-stu-id="2a9fa-109">The string must be in the following format so that clients can easily parse it: \[\[modifier key\]+\[...\]+\] key name.</span></span>

<span data-ttu-id="2a9fa-110">範例包括 ALT + F、CTRL + ALT + 4、WIN + F1、CTRL + ALT + SHIFT + 倒退鍵或單純倒退鍵。</span><span class="sxs-lookup"><span data-stu-id="2a9fa-110">Examples include ALT+F, CTRL+ALT+4, WIN+F1, CTRL+ALT+SHIFT+BACKSPACE, or simply BACKSPACE.</span></span>

<span data-ttu-id="2a9fa-111">下表列出輔助按鍵。</span><span class="sxs-lookup"><span data-stu-id="2a9fa-111">The following table lists modifier keys.</span></span>



| <span data-ttu-id="2a9fa-112">輔助按鍵</span><span class="sxs-lookup"><span data-stu-id="2a9fa-112">Modifier key</span></span> | <span data-ttu-id="2a9fa-113">Description</span><span class="sxs-lookup"><span data-stu-id="2a9fa-113">Description</span></span>                        |
|--------------|------------------------------------|
| <span data-ttu-id="2a9fa-114">ALT</span><span class="sxs-lookup"><span data-stu-id="2a9fa-114">ALT</span></span>          | <span data-ttu-id="2a9fa-115">替代輔助按鍵</span><span class="sxs-lookup"><span data-stu-id="2a9fa-115">Alternate modifier key</span></span>             |
| <span data-ttu-id="2a9fa-116">CTRL</span><span class="sxs-lookup"><span data-stu-id="2a9fa-116">CTRL</span></span>         | <span data-ttu-id="2a9fa-117">控制輔助按鍵</span><span class="sxs-lookup"><span data-stu-id="2a9fa-117">Control modifier key</span></span>               |
| <span data-ttu-id="2a9fa-118">SHIFT</span><span class="sxs-lookup"><span data-stu-id="2a9fa-118">SHIFT</span></span>        | <span data-ttu-id="2a9fa-119">Shift 輔助按鍵</span><span class="sxs-lookup"><span data-stu-id="2a9fa-119">Shift modifier key</span></span>                 |
| <span data-ttu-id="2a9fa-120">贏得</span><span class="sxs-lookup"><span data-stu-id="2a9fa-120">WIN</span></span>          | <span data-ttu-id="2a9fa-121">Windows 標誌鍵</span><span class="sxs-lookup"><span data-stu-id="2a9fa-121">Windows logo key</span></span>                   |
| <span data-ttu-id="2a9fa-122">FN</span><span class="sxs-lookup"><span data-stu-id="2a9fa-122">FN</span></span>           | <span data-ttu-id="2a9fa-123">可攜式電腦上的功能機碼</span><span class="sxs-lookup"><span data-stu-id="2a9fa-123">Function key on portable computers</span></span> |



 

<span data-ttu-id="2a9fa-124">請勿當地語系化鍵盤快速鍵字串。</span><span class="sxs-lookup"><span data-stu-id="2a9fa-124">Do not localize keyboard shortcut strings.</span></span>

## <a name="handling-objects-that-have-both-key-types"></a><span data-ttu-id="2a9fa-125">處理具有兩個索引鍵類型的物件</span><span class="sxs-lookup"><span data-stu-id="2a9fa-125">Handling Objects That Have Both Key Types</span></span>

<span data-ttu-id="2a9fa-126">如果物件同時具有快速鍵和存取金鑰， **KeyboardShortcut** 屬性會傳回存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="2a9fa-126">If an object has both a shortcut key and an access key, the **KeyboardShortcut** property returns the access key.</span></span> <span data-ttu-id="2a9fa-127">存取金鑰是當物件或物件的父系具有鍵盤焦點時，使用者會按下的按鍵。</span><span class="sxs-lookup"><span data-stu-id="2a9fa-127">The access key is the one a user would press when the object or the object's parent has the keyboard focus.</span></span> <span data-ttu-id="2a9fa-128">例如，[ **列印** ] 功能表項目可能會同時有快速鍵 (CTRL + P) 和 (P) 的存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="2a9fa-128">For example, the **Print** menu item might have both a shortcut key (CTRL+P) and an access key (P).</span></span> <span data-ttu-id="2a9fa-129">如果使用者在功能表使用中時按 CTRL + P，就不會發生任何事。</span><span class="sxs-lookup"><span data-stu-id="2a9fa-129">If a user presses CTRL+P while the menu is active, nothing happens.</span></span> <span data-ttu-id="2a9fa-130">但是，如果使用者在功能表使用中時按 P，就會叫用應用程式的 [ **列印** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="2a9fa-130">But if a user presses P while the menu is active, it invokes the application's **Print** dialog box.</span></span> <span data-ttu-id="2a9fa-131">在此情況下， **KeyboardShortcut** 屬性為 "P"，以反映當功能表具有鍵盤焦點時，使用者必須按下的內容。</span><span class="sxs-lookup"><span data-stu-id="2a9fa-131">In this case, the **KeyboardShortcut** property is "P" to reflect what the user must press when the menu has the keyboard focus.</span></span>

 

 




