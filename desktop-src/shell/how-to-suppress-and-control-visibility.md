---
description: 本主題將告訴您如何控制動詞可視性。
title: 如何隱藏和控制動詞可見度
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f689d8b93ce9facb62b654f3f8be62f665e001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192682"
---
# <a name="how-to-suppress-and-control-verb-visibility"></a><span data-ttu-id="f1db2-103">如何隱藏和控制動詞可見度</span><span class="sxs-lookup"><span data-stu-id="f1db2-103">How to Suppress and Control Verb Visibility</span></span>

<span data-ttu-id="f1db2-104">本主題將告訴您如何控制動詞可視性。</span><span class="sxs-lookup"><span data-stu-id="f1db2-104">This topic tells you how to control verb visibility.</span></span>

## <a name="instructions"></a><span data-ttu-id="f1db2-105">指示</span><span class="sxs-lookup"><span data-stu-id="f1db2-105">Instructions</span></span>


<span data-ttu-id="f1db2-106">您可以使用 Windows 原則設定來控制動詞可視性。</span><span class="sxs-lookup"><span data-stu-id="f1db2-106">You can use Windows policy settings to control verb visibility.</span></span> <span data-ttu-id="f1db2-107">藉由將 **SuppressionPolicy** 子機碼或 **SuppressionPolicyEx** GUID 值新增至動詞的登錄子機碼，就可以透過原則設定來隱藏動詞命令。</span><span class="sxs-lookup"><span data-stu-id="f1db2-107">Verbs can be suppressed through policy settings by adding a **SuppressionPolicy** subkey or a **SuppressionPolicyEx** GUID value to the verb's registry subkey.</span></span> <span data-ttu-id="f1db2-108">將 **SuppressionPolicy** 子機碼的值設定為原則識別碼。</span><span class="sxs-lookup"><span data-stu-id="f1db2-108">Set the value of the **SuppressionPolicy** subkey to the policy ID.</span></span> <span data-ttu-id="f1db2-109">如果原則已開啟，則會隱藏動詞和其相關聯的快捷方式功能表項目。</span><span class="sxs-lookup"><span data-stu-id="f1db2-109">If the policy is turned on, the verb and its associated shortcut menu entry are suppressed.</span></span> <span data-ttu-id="f1db2-110">如需可能的原則識別碼值，請參閱 [**限制**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) 列舉。</span><span class="sxs-lookup"><span data-stu-id="f1db2-110">For possible policy ID values, see the [**RESTRICTIONS**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) enumeration.</span></span>

 

 



