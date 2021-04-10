---
title: readonly 屬性
description: '\ Readonly \ 屬性禁止指派給變數。'
ms.assetid: b81064e6-e788-48d1-9958-203f1e3c7e4d
keywords:
- readonly 屬性 MIDL
topic_type:
- apiref
api_name:
- readonly
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b4ef4ca5f32b96146ed5ab0ec085d32b24dca3a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933190"
---
# <a name="readonly-attribute"></a><span data-ttu-id="5223e-104">readonly 屬性</span><span class="sxs-lookup"><span data-stu-id="5223e-104">readonly attribute</span></span>

<span data-ttu-id="5223e-105">**\[ Readonly \]** 屬性禁止指派給變數。</span><span class="sxs-lookup"><span data-stu-id="5223e-105">The **\[readonly\]** attribute prohibits assignment to a variable.</span></span>

``` syntax
[readonly [, optional-attributes]] data-type identifier
```

## <a name="parameters"></a><span data-ttu-id="5223e-106">參數</span><span class="sxs-lookup"><span data-stu-id="5223e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5223e-107">*選用-屬性*</span><span class="sxs-lookup"><span data-stu-id="5223e-107">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="5223e-108">零或多個 MIDL 屬性。</span><span class="sxs-lookup"><span data-stu-id="5223e-108">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="5223e-109">*資料類型*</span><span class="sxs-lookup"><span data-stu-id="5223e-109">*data-type*</span></span> 
</dt> <dd>

<span data-ttu-id="5223e-110">*識別碼* 所包含的資料類型。</span><span class="sxs-lookup"><span data-stu-id="5223e-110">The type of the data contained by *identifier*.</span></span>

</dd> <dt>

<span data-ttu-id="5223e-111">*identifier*</span><span class="sxs-lookup"><span data-stu-id="5223e-111">*identifier*</span></span> 
</dt> <dd>

<span data-ttu-id="5223e-112">軟體可參考資料儲存位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="5223e-112">A name by which the software can refer to the data storage location.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5223e-113">備註</span><span class="sxs-lookup"><span data-stu-id="5223e-113">Remarks</span></span>

<span data-ttu-id="5223e-114">**\[ Readonly \]** 屬性禁止指派給變數。</span><span class="sxs-lookup"><span data-stu-id="5223e-114">The **\[readonly\]** attribute prohibits assignment to a variable.</span></span> <span data-ttu-id="5223e-115">只有在參數層級才支援 **\[ readonly \]** ，而不是在方法層級支援。</span><span class="sxs-lookup"><span data-stu-id="5223e-115">**\[readonly\]** is only supported at the parameter level, not at the method level.</span></span>

### <a name="flags"></a><span data-ttu-id="5223e-116">Flags</span><span class="sxs-lookup"><span data-stu-id="5223e-116">Flags</span></span>

<span data-ttu-id="5223e-117">VARFLAG \_ FREADONLY</span><span class="sxs-lookup"><span data-stu-id="5223e-117">VARFLAG\_FREADONLY</span></span>

## <a name="examples"></a><span data-ttu-id="5223e-118">範例</span><span class="sxs-lookup"><span data-stu-id="5223e-118">Examples</span></span>

``` syntax
HRESULT Method3([in, readonly] int iMmutable);
```

## <a name="see-also"></a><span data-ttu-id="5223e-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5223e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5223e-120">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="5223e-120">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="5223e-121">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="5223e-121">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="5223e-122">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="5223e-122">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="5223e-123">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="5223e-123">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 