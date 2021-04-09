---
title: ncacn_at_dsp 屬性
description: Ncacn \_ at \_ dsp 關鍵字會將 AppleTalk dsp 識別為端點的通訊協定系列。 此通訊協定系列已淘汰，不應在新的應用程式中使用。
ms.assetid: 3165e4f6-8869-4eff-af65-53e85f78a949
keywords:
- ncacn_at_dsp 屬性 MIDL
topic_type:
- apiref
api_name:
- ncacn_at_dsp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9149cd7270c2e82e760c24b4af1fed54c2c08622
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933201"
---
# <a name="ncacn_at_dsp-attribute"></a><span data-ttu-id="c4a6b-105">ncacn \_ 于 \_ dsp 屬性</span><span class="sxs-lookup"><span data-stu-id="c4a6b-105">ncacn\_at\_dsp attribute</span></span>

<span data-ttu-id="c4a6b-106">**Ncacn \_ at \_ dsp** 關鍵字會將 AppleTalk dsp 識別為端點的通訊協定系列。</span><span class="sxs-lookup"><span data-stu-id="c4a6b-106">The **ncacn\_at\_dsp** keyword identifies AppleTalk DSP as the protocol family for the endpoint.</span></span> <span data-ttu-id="c4a6b-107">此通訊協定系列已淘汰，不應在新的應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="c4a6b-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_at_dsp:[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="c4a6b-108">參數</span><span class="sxs-lookup"><span data-stu-id="c4a6b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4a6b-109">*埠名稱*</span><span class="sxs-lookup"><span data-stu-id="c4a6b-109">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="c4a6b-110">指定長度最多為22個位元組的字元字串。</span><span class="sxs-lookup"><span data-stu-id="c4a6b-110">Specifies a character string up to 22 bytes long.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4a6b-111">備註</span><span class="sxs-lookup"><span data-stu-id="c4a6b-111">Remarks</span></span>

<span data-ttu-id="c4a6b-112">AppleTalk DSP 埠字串的語法（如同所有的埠字串）是由傳輸執行所定義，而且與 IDL 規格無關。</span><span class="sxs-lookup"><span data-stu-id="c4a6b-112">The syntax of the AppleTalk DSP port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="c4a6b-113">MIDL 編譯器會執行有限的語法檢查，但不保證端點規格是正確的。</span><span class="sxs-lookup"><span data-stu-id="c4a6b-113">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="c4a6b-114">某些錯誤類別可能會在執行時間（而不是在編譯時期）回報。</span><span class="sxs-lookup"><span data-stu-id="c4a6b-114">Some classes of errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="c4a6b-115">範例</span><span class="sxs-lookup"><span data-stu-id="c4a6b-115">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_at_dsp:[my_services_endpoint]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="c4a6b-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c4a6b-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4a6b-117">**端點**</span><span class="sxs-lookup"><span data-stu-id="c4a6b-117">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="c4a6b-118"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="c4a6b-118">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="c4a6b-119">**字串系結**</span><span class="sxs-lookup"><span data-stu-id="c4a6b-119">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 