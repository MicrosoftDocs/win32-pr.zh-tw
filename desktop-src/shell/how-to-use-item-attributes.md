---
description: 您可以測試專案之 Shell 屬性的 SFGAO 旗標值，以判斷是否應啟用或停用動詞。
ms.assetid: 3A539A9D-DB6B-4E3D-AD26-D5309BECEBB1
title: 如何使用專案屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a438c81258677822ca9b940eb9f74366d6226ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849188"
---
# <a name="how-to-use-item-attributes"></a><span data-ttu-id="e86b3-103">如何使用專案屬性</span><span class="sxs-lookup"><span data-stu-id="e86b3-103">How to Use Item Attributes</span></span>

<span data-ttu-id="e86b3-104">您可以測試專案之 Shell 屬性的 [**SFGAO**](sfgao.md) 旗標值，以判斷是否應啟用或停用動詞。</span><span class="sxs-lookup"><span data-stu-id="e86b3-104">The [**SFGAO**](sfgao.md) flag values of the Shell attributes for an item can be tested to determine whether the verb should be enabled or disabled.</span></span>

<span data-ttu-id="e86b3-105">若要使用此屬性功能，請在動詞命令底下新增下列 **REG \_ DWORD** 值：</span><span class="sxs-lookup"><span data-stu-id="e86b3-105">To use this attribute feature, add the following **REG\_DWORD** values under the verb:</span></span>

## <a name="instructions"></a><span data-ttu-id="e86b3-106">指示</span><span class="sxs-lookup"><span data-stu-id="e86b3-106">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="e86b3-107">步驟 1:</span><span class="sxs-lookup"><span data-stu-id="e86b3-107">Step 1:</span></span>

<span data-ttu-id="e86b3-108">AttributeMask 值會指定要測試之遮罩的位值 [**SFGAO**](sfgao.md) 值。</span><span class="sxs-lookup"><span data-stu-id="e86b3-108">The AttributeMask value specifies the [**SFGAO**](sfgao.md) value of the bit values of the mask to test with.</span></span>

### <a name="step-2"></a><span data-ttu-id="e86b3-109">步驟 2:</span><span class="sxs-lookup"><span data-stu-id="e86b3-109">Step 2:</span></span>

<span data-ttu-id="e86b3-110">AttributeValue 值會指定所測試之位的 [**SFGAO**](sfgao.md) 值。</span><span class="sxs-lookup"><span data-stu-id="e86b3-110">The AttributeValue value specifies the [**SFGAO**](sfgao.md) value of the bits that are tested.</span></span>

### <a name="step-3"></a><span data-ttu-id="e86b3-111">步驟 3：</span><span class="sxs-lookup"><span data-stu-id="e86b3-111">Step 3:</span></span>

<span data-ttu-id="e86b3-112">ImpliedSelectionModel 為專案動詞指定零，或在背景快捷方式功能表上指定非零的動詞。</span><span class="sxs-lookup"><span data-stu-id="e86b3-112">The ImpliedSelectionModel specifies zero for item verbs, or nonzero for verbs on the background shortcut menu.</span></span>

## <a name="remarks"></a><span data-ttu-id="e86b3-113">備註</span><span class="sxs-lookup"><span data-stu-id="e86b3-113">Remarks</span></span>

<span data-ttu-id="e86b3-114">在下列範例登錄專案中，AttributeMask 會設定為 [**SFGAO \_ READONLY**](sfgao.md) (0x40000) 。</span><span class="sxs-lookup"><span data-stu-id="e86b3-114">In the following example registry entry, the AttributeMask is set to [**SFGAO\_READONLY**](sfgao.md) (0x40000).</span></span>

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         test.verb2
            AttributeMask = 0x40000
            AttributeValue = 0x0
            ImpliedSelectionModel = 0x0
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

 

 



