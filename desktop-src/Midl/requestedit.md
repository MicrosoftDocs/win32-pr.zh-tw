---
title: requestedit 屬性
description: '\ Requestedit \ 屬性工作表示屬性支援 OnRequestEdit 通知。'
ms.assetid: 63f38d83-596b-4031-bb6a-972374cd0c60
keywords:
- requestedit 屬性 MIDL
topic_type:
- apiref
api_name:
- requestedit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18d83beea34f008e6e96fcd493d8410d7d2c5b88
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106965231"
---
# <a name="requestedit-attribute"></a><span data-ttu-id="01e3e-104">requestedit 屬性</span><span class="sxs-lookup"><span data-stu-id="01e3e-104">requestedit attribute</span></span>

<span data-ttu-id="01e3e-105">**\[ Requestedit \]** 屬性指出屬性支援 **OnRequestEdit** 通知。</span><span class="sxs-lookup"><span data-stu-id="01e3e-105">The **\[requestedit\]** attribute indicates that the property supports the **OnRequestEdit** notification.</span></span>

``` syntax
[requestedit [,optional-attributes]] return-type function-name(params)
```

## <a name="parameters"></a><span data-ttu-id="01e3e-106">參數</span><span class="sxs-lookup"><span data-stu-id="01e3e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01e3e-107">*選用-屬性*</span><span class="sxs-lookup"><span data-stu-id="01e3e-107">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="01e3e-108">零或多個 MIDL 屬性。</span><span class="sxs-lookup"><span data-stu-id="01e3e-108">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="01e3e-109">*傳回類型*</span><span class="sxs-lookup"><span data-stu-id="01e3e-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="01e3e-110">指定函式的傳回型別。</span><span class="sxs-lookup"><span data-stu-id="01e3e-110">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="01e3e-111">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="01e3e-111">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="01e3e-112">在 IDL 檔案中指定函數的名稱。</span><span class="sxs-lookup"><span data-stu-id="01e3e-112">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="01e3e-113">*params*</span><span class="sxs-lookup"><span data-stu-id="01e3e-113">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="01e3e-114">零或多個函數參數。</span><span class="sxs-lookup"><span data-stu-id="01e3e-114">Zero or more function parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="01e3e-115">備註</span><span class="sxs-lookup"><span data-stu-id="01e3e-115">Remarks</span></span>

<span data-ttu-id="01e3e-116">支援 **OnRequestEdit** 通知表示在進行變更之前，物件會將變更屬性之許可權的要求傳送給用戶端。</span><span class="sxs-lookup"><span data-stu-id="01e3e-116">Supporting **OnRequestEdit** notification means that, before a change is made, the object will send the client a request for permission to change a property.</span></span> <span data-ttu-id="01e3e-117">物件可以支援資料系結，但不能有這個屬性。</span><span class="sxs-lookup"><span data-stu-id="01e3e-117">An object can support data binding but not have this attribute.</span></span>

### <a name="flags"></a><span data-ttu-id="01e3e-118">Flags</span><span class="sxs-lookup"><span data-stu-id="01e3e-118">Flags</span></span>

<span data-ttu-id="01e3e-119">FUNCFLAG \_ FREQUESTEDIT、VARFLAG \_ FREQUESTEDIT</span><span class="sxs-lookup"><span data-stu-id="01e3e-119">FUNCFLAG\_FREQUESTEDIT, VARFLAG\_FREQUESTEDIT</span></span>

## <a name="examples"></a><span data-ttu-id="01e3e-120">範例</span><span class="sxs-lookup"><span data-stu-id="01e3e-120">Examples</span></span>

``` syntax
properties:
    [propget, helpstring("A useful comment"), bindable, defaultbind,
     displaybind, requestedit] long Func1(void);
```

## <a name="see-also"></a><span data-ttu-id="01e3e-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="01e3e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01e3e-122">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="01e3e-122">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="01e3e-123">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="01e3e-123">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="01e3e-124">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="01e3e-124">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="01e3e-125">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="01e3e-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 