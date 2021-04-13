---
title: /oldtlb 參數
description: /Oldtlb 參數會指示 MIDL 編譯器產生舊格式的類型程式庫。
ms.assetid: cf5fe000-7262-4812-a6ab-f12a558ac068
keywords:
- /oldtlb 參數 MIDL
topic_type:
- apiref
api_name:
- /oldtlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a08e468d0acff16aa1df4a45fcacafeb676b00
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375085"
---
# <a name="oldtlb-switch"></a><span data-ttu-id="1b08b-104">/oldtlb 參數</span><span class="sxs-lookup"><span data-stu-id="1b08b-104">/oldtlb switch</span></span>

<span data-ttu-id="1b08b-105">**/Oldtlb** 參數會指示 MIDL 編譯器產生舊格式的類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="1b08b-105">The **/oldtlb** switch directs the MIDL compiler to generate an old-format type library.</span></span>

``` syntax
midl /oldtlb
```

## <a name="switch-options"></a><span data-ttu-id="1b08b-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="1b08b-106">Switch Options</span></span>

<span data-ttu-id="1b08b-107">此參數沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="1b08b-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b08b-108">備註</span><span class="sxs-lookup"><span data-stu-id="1b08b-108">Remarks</span></span>

<span data-ttu-id="1b08b-109">**/Oldtlb** 參數會覆寫預設值，並指示 MIDL 編譯器在目前的 Windows 版本上，使用 [CreateTypeLib](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib)而不是 [CreateTypeLib2](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib2)來產生舊格式的類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="1b08b-109">The **/oldtlb** switch overrides the default and directs the MIDL compiler to generate old-format type libraries even on current versions of Windows by using [CreateTypeLib](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib) instead of [CreateTypeLib2](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib2).</span></span>

## <a name="examples"></a><span data-ttu-id="1b08b-110">範例</span><span class="sxs-lookup"><span data-stu-id="1b08b-110">Examples</span></span>

<span data-ttu-id="1b08b-111">**midl/oldtlb 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="1b08b-111">**midl /oldtlb filename.idl**</span></span>

<span data-ttu-id="1b08b-112">**midl/oldtlb myoldodl. odl**</span><span class="sxs-lookup"><span data-stu-id="1b08b-112">**midl /oldtlb myoldodl.odl**</span></span>

## <a name="see-also"></a><span data-ttu-id="1b08b-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1b08b-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b08b-114">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="1b08b-114">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="1b08b-115">**/newtlb**</span><span class="sxs-lookup"><span data-stu-id="1b08b-115">**/newtlb**</span></span>](-newtlb.md)
</dt> </dl>

 

 