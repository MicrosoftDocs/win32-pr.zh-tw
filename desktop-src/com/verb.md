---
title: 動詞命令
description: 指定要為應用程式註冊的動詞。
ms.assetid: bfcad36d-a52a-4117-bf0b-6135b197a7ee
keywords:
- 動詞登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ef025ee0807ca3e75577f26f81951db22dfb0ac
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106966889"
---
# <a name="verb"></a><span data-ttu-id="e3cbb-104">動詞命令</span><span class="sxs-lookup"><span data-stu-id="e3cbb-104">Verb</span></span>

<span data-ttu-id="e3cbb-105">指定要為應用程式註冊的動詞。</span><span class="sxs-lookup"><span data-stu-id="e3cbb-105">Specifies the verbs to be registered for an application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="e3cbb-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="e3cbb-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Verb
         1 = verb1
         2 = verb2
         3 = ...
```

## <a name="remarks"></a><span data-ttu-id="e3cbb-107">備註</span><span class="sxs-lookup"><span data-stu-id="e3cbb-107">Remarks</span></span>

<span data-ttu-id="e3cbb-108">每個動詞都是以「*名稱*」、「*功能表 \_ 旗* 標」、「*動詞 \_ 旗* 標」形式的 **REG \_ SZ** 值。</span><span class="sxs-lookup"><span data-stu-id="e3cbb-108">Each verb is a **REG\_SZ** value of the form "*name*, *menu\_flag*, *verb\_flag*".</span></span> <span data-ttu-id="e3cbb-109">動詞必須是連續的編號。</span><span class="sxs-lookup"><span data-stu-id="e3cbb-109">Verbs must be numbered consecutively.</span></span>

<span data-ttu-id="e3cbb-110">此 *名稱* 描述 [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) 函式呼叫如何附加動詞。</span><span class="sxs-lookup"><span data-stu-id="e3cbb-110">The *name* describes how the verb is appended by an [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) function call.</span></span> <span data-ttu-id="e3cbb-111">例如「&Play」。</span><span class="sxs-lookup"><span data-stu-id="e3cbb-111">For example, "&Play".</span></span>

<span data-ttu-id="e3cbb-112">*功能表 \_ 旗* 標值會指出動詞應該如何出現在功能表中。</span><span class="sxs-lookup"><span data-stu-id="e3cbb-112">The *menu\_flag* value indicates how the verb should appear in the menu.</span></span> <span data-ttu-id="e3cbb-113">除了 MF [](/windows/win32/api/winuser/nf-winuser-appendmenua) \_ BITMAP、MF \_ OWNERDRAW 和 MF 快顯視窗以外，支援 AppendMenu 支援的所有旗標 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e3cbb-113">All flags supported by [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) are supported, except for MF\_BITMAP, MF\_OWNERDRAW, and MF\_POPUP.</span></span>

<span data-ttu-id="e3cbb-114">*動詞 \_ 旗* 標值描述動詞的屬性。</span><span class="sxs-lookup"><span data-stu-id="e3cbb-114">The *verb\_flag* value describes attributes of the verbs.</span></span> <span data-ttu-id="e3cbb-115">使用 [**OLEVERBATTRIB**](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)中的其中一個值，或0。</span><span class="sxs-lookup"><span data-stu-id="e3cbb-115">Use one of the values from [**OLEVERBATTRIB**](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib), or 0.</span></span>

<span data-ttu-id="e3cbb-116">如需詳細資訊，請參閱 [**OLEVERB**](/windows/win32/api/oleidl/ns-oleidl-oleverb)、 [**IOleObject：:D overb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb)和 [**IOleObject：： EnumVerbs**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-enumverbs)。</span><span class="sxs-lookup"><span data-stu-id="e3cbb-116">For more information, see [**OLEVERB**](/windows/win32/api/oleidl/ns-oleidl-oleverb), [**IOleObject::DoVerb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb), and [**IOleObject::EnumVerbs**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-enumverbs).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3cbb-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="e3cbb-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3cbb-118">**AppendMenu**</span><span class="sxs-lookup"><span data-stu-id="e3cbb-118">**AppendMenu**</span></span>](/windows/win32/api/winuser/nf-winuser-appendmenua)
</dt> <dt>

[<span data-ttu-id="e3cbb-119">**OLEVERB**</span><span class="sxs-lookup"><span data-stu-id="e3cbb-119">**OLEVERB**</span></span>](/windows/win32/api/oleidl/ns-oleidl-oleverb)
</dt> <dt>

[<span data-ttu-id="e3cbb-120">**OLEVERBATTRIB**</span><span class="sxs-lookup"><span data-stu-id="e3cbb-120">**OLEVERBATTRIB**</span></span>](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)
</dt> </dl>

 

 