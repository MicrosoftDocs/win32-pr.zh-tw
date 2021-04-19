---
description: IME 會執行一個稱為 &0034 的功能 \# ; 將&\# 0034;。
ms.assetid: 32b20872-7e5c-487e-99bb-9447ac3aebd4
title: 搭配 IME 使用漢字重組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e28383a27fd7fd7827cbbf3c7ff97c895fb4a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973997"
---
# <a name="using-reconversion-with-an-ime"></a><span data-ttu-id="6b750-103">搭配 IME 使用漢字重組</span><span class="sxs-lookup"><span data-stu-id="6b750-103">Using Reconversion with an IME</span></span>

<span data-ttu-id="6b750-104">IME 會執行稱為「漢字重組」的功能。</span><span class="sxs-lookup"><span data-stu-id="6b750-104">An IME implements a feature called "reconversion".</span></span> <span data-ttu-id="6b750-105">一般而言，IMM 只會根據使用者輸入的專案來判斷候選清單。</span><span class="sxs-lookup"><span data-stu-id="6b750-105">Normally the IMM determines the lists of candidates based only on entries typed by the user.</span></span> <span data-ttu-id="6b750-106">[重設] 可讓 IMM 根據內容)  (包含的句子，判斷一或多個候選項目。</span><span class="sxs-lookup"><span data-stu-id="6b750-106">Reconversion allows the IMM to determine one or more candidates based on the containing sentence (the context).</span></span> <span data-ttu-id="6b750-107">定義的重組類型很簡單、正常且增強。</span><span class="sxs-lookup"><span data-stu-id="6b750-107">The defined reconversion types are simple, normal, and enhanced.</span></span>

<span data-ttu-id="6b750-108">當使用者在檔中注意到組合錯誤時，「重做」會很有用。</span><span class="sxs-lookup"><span data-stu-id="6b750-108">Reconversion is useful when a user notices a composition error in a document.</span></span> <span data-ttu-id="6b750-109">使用者可以選取該錯誤，然後從功能表中選擇 [重組]。</span><span class="sxs-lookup"><span data-stu-id="6b750-109">The user can select the error and choose reconversion from a menu.</span></span> <span data-ttu-id="6b750-110">IME 會使用內容來判斷最佳的取代。</span><span class="sxs-lookup"><span data-stu-id="6b750-110">The IME uses the context to determine the best replacement.</span></span> <span data-ttu-id="6b750-111">應用程式可以使用 [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) 來支援重組。</span><span class="sxs-lookup"><span data-stu-id="6b750-111">The application can use [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) to support reconversion.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b750-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="6b750-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b750-113">使用輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="6b750-113">Using Input Method Manager</span></span>](using-input-method-manager.md)
</dt> </dl>

 

 



