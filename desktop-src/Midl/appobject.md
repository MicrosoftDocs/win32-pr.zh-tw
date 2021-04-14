---
title: appobject 屬性
description: '\ Appobject \ 屬性會將 coclass 識別為應用程式物件，此物件與完整 EXE 應用程式相關聯。'
ms.assetid: f4fcdf55-7431-4d66-8a46-f741c52fbe56
keywords:
- appobject 屬性 MIDL
topic_type:
- apiref
api_name:
- appobject
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0d937d4a83306bc0c29f3c8c806bc043febec6a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375084"
---
# <a name="appobject-attribute"></a><span data-ttu-id="adfe5-104">appobject 屬性</span><span class="sxs-lookup"><span data-stu-id="adfe5-104">appobject attribute</span></span>

<span data-ttu-id="adfe5-105">**\[ Appobject \]** 屬性會將 [**coclass**](coclass.md)識別為應用程式物件，此物件與完整 EXE 應用程式相關聯。</span><span class="sxs-lookup"><span data-stu-id="adfe5-105">The **\[appobject\]** attribute identifies the [**coclass**](coclass.md) as an application object, which is associated with a full EXE application.</span></span>

``` syntax
[
    uuid(uuid-number), 
    appobject 
  [, coclass-attribute-list]
]
coclass classname 
{ 
    [coclass definition]
}
```

## <a name="parameters"></a><span data-ttu-id="adfe5-106">參數</span><span class="sxs-lookup"><span data-stu-id="adfe5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adfe5-107">*uuid-數位*</span><span class="sxs-lookup"><span data-stu-id="adfe5-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="adfe5-108">指定 [**coclass**](coclass.md)的通用唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="adfe5-108">Specifies a universally unique identification number for the [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="adfe5-109">*coclass-屬性清單*</span><span class="sxs-lookup"><span data-stu-id="adfe5-109">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="adfe5-110">指定套用至 [**coclass**](coclass.md) 語句的零或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="adfe5-110">Specifies zero or more attributes that apply to the [**coclass**](coclass.md) statement.</span></span> <span data-ttu-id="adfe5-111">允許 **的 coclass** 屬性為 [**\[ helpstring \]**](helpstring.md)、 [**\[ helpcoNtext \]**](helpcontext.md)、 [**\[ 授權 \]**](licensed.md)、 [**\[ 版本 \]**](version.md)、 [**\[ 控制項 \]**](control.md)和 [**\[ 隱藏 \]**](hidden.md)。</span><span class="sxs-lookup"><span data-stu-id="adfe5-111">Allowable **coclass** attributes are [**\[helpstring\]**](helpstring.md), [**\[helpcontext\]**](helpcontext.md), [**\[licensed\]**](licensed.md), [**\[version\]**](version.md), [**\[control\]**](control.md), and [**\[hidden\]**](hidden.md).</span></span>

</dd> <dt>

<span data-ttu-id="adfe5-112">*classname*</span><span class="sxs-lookup"><span data-stu-id="adfe5-112">*classname*</span></span> 
</dt> <dd>

<span data-ttu-id="adfe5-113">指定在類型程式庫中已知元件物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="adfe5-113">Specifies the name by which the component object is known in the type library.</span></span>

</dd> <dt>

<span data-ttu-id="adfe5-114">*coclass 定義*</span><span class="sxs-lookup"><span data-stu-id="adfe5-114">*coclass definition*</span></span> 
</dt> <dd>

<span data-ttu-id="adfe5-115">指定組成 [**coclass**](coclass.md) 定義的語句。</span><span class="sxs-lookup"><span data-stu-id="adfe5-115">Specifies statements that make up the [**coclass**](coclass.md) definition.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="adfe5-116">備註</span><span class="sxs-lookup"><span data-stu-id="adfe5-116">Remarks</span></span>

<span data-ttu-id="adfe5-117">**\[ Appobject \]** 屬性也表示 [**coclass**](coclass.md)的函式和屬性在目前的類型程式庫中為全域可用。</span><span class="sxs-lookup"><span data-stu-id="adfe5-117">The **\[appobject\]** attribute also indicates that the functions and properties of the [**coclass**](coclass.md) are globally available in the current type library.</span></span>

<span data-ttu-id="adfe5-118">這個屬性的 typeflag 標記法為 TYPEFLAG \_ FAPPOBJECT</span><span class="sxs-lookup"><span data-stu-id="adfe5-118">The typeflag representation for this attribute is TYPEFLAG\_FAPPOBJECT</span></span>

## <a name="examples"></a><span data-ttu-id="adfe5-119">範例</span><span class="sxs-lookup"><span data-stu-id="adfe5-119">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("Hello Class"),
    appobject
] 
coclass Hello
{
    [default] interface IHello : IUnknown;
    interface IDispatch;
}
```

## <a name="see-also"></a><span data-ttu-id="adfe5-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="adfe5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adfe5-121">**coclass**</span><span class="sxs-lookup"><span data-stu-id="adfe5-121">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="adfe5-122">**控制**</span><span class="sxs-lookup"><span data-stu-id="adfe5-122">**control**</span></span>](control.md)
</dt> <dt>

[<span data-ttu-id="adfe5-123">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="adfe5-123">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="adfe5-124">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="adfe5-124">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="adfe5-125">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="adfe5-125">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="adfe5-126">**隱藏**</span><span class="sxs-lookup"><span data-stu-id="adfe5-126">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="adfe5-127">**licensed**</span><span class="sxs-lookup"><span data-stu-id="adfe5-127">**licensed**</span></span>](licensed.md)
</dt> <dt>

[<span data-ttu-id="adfe5-128">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="adfe5-128">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="adfe5-129">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="adfe5-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="adfe5-130">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="adfe5-130">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="adfe5-131">**版本**</span><span class="sxs-lookup"><span data-stu-id="adfe5-131">**version**</span></span>](version.md)
</dt> </dl>

 

 