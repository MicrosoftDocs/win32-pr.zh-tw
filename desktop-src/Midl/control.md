---
title: control 屬性
description: '\ Control \ 屬性會將 coclass 或程式庫識別為 COM 控制項，以供容器網站衍生其他型別程式庫或元件物件類別。'
ms.assetid: c39dd4b6-743f-4888-8954-8b83584bdea5
keywords:
- control 屬性 MIDL
topic_type:
- apiref
api_name:
- control
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 982327d581ddb606f733e9efbbcb89e2f9972cf4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681771"
---
# <a name="control-attribute"></a><span data-ttu-id="80a8c-104">control 屬性</span><span class="sxs-lookup"><span data-stu-id="80a8c-104">control attribute</span></span>

<span data-ttu-id="80a8c-105">**\[ 控制項 \]** 屬性會將 [**coclass**](coclass.md)或連結 [**庫**](library.md)識別為 COM 控制項，容器網站會從中衍生其他型別程式庫或元件物件類別。</span><span class="sxs-lookup"><span data-stu-id="80a8c-105">The **\[control\]** attribute identifies a [**coclass**](coclass.md) or [**library**](library.md) as a COM control, from which a container site will derive additional type libraries or component object classes.</span></span>

``` syntax
[
    uuid, 
    control 
    [, attribute-list]
] 
library | coclass lib-or-coclassname 
{ 
    definitions 
}
```

## <a name="parameters"></a><span data-ttu-id="80a8c-106">參數</span><span class="sxs-lookup"><span data-stu-id="80a8c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80a8c-107">*屬性清單*</span><span class="sxs-lookup"><span data-stu-id="80a8c-107">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="80a8c-108">指定適用于連結 [**庫**](library.md) 或 [**coclass**](coclass.md) 語句的零或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="80a8c-108">Specifies zero or more attributes that apply to the [**library**](library.md) or [**coclass**](coclass.md) statement.</span></span> <span data-ttu-id="80a8c-109">以逗號分隔多個屬性。</span><span class="sxs-lookup"><span data-stu-id="80a8c-109">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="80a8c-110">*lib 或-coclassname*</span><span class="sxs-lookup"><span data-stu-id="80a8c-110">*lib-or-coclassname*</span></span> 
</dt> <dd>

<span data-ttu-id="80a8c-111">指定連結 [**庫**](library.md) 或 [**coclass**](coclass.md)的名稱。</span><span class="sxs-lookup"><span data-stu-id="80a8c-111">Specifies the name of the [**library**](library.md) or [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="80a8c-112">*定義*</span><span class="sxs-lookup"><span data-stu-id="80a8c-112">*definitions*</span></span> 
</dt> <dd>

<span data-ttu-id="80a8c-113">MIDL 語句，可指定連結 [**庫**](library.md) 或 [**coclass**](coclass.md)的成員。</span><span class="sxs-lookup"><span data-stu-id="80a8c-113">MIDL statements that specify the members of the [**library**](library.md) or [**coclass**](coclass.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="80a8c-114">備註</span><span class="sxs-lookup"><span data-stu-id="80a8c-114">Remarks</span></span>

<span data-ttu-id="80a8c-115">這個屬性可讓您標記描述控制項的類型程式庫，使其不會顯示在適用于非視覺化物件的型別瀏覽器中。</span><span class="sxs-lookup"><span data-stu-id="80a8c-115">This attribute allows you to mark type libraries that describe controls so they will not be displayed in type browsers intended for nonvisual objects.</span></span>

### <a name="flags"></a><span data-ttu-id="80a8c-116">Flags</span><span class="sxs-lookup"><span data-stu-id="80a8c-116">Flags</span></span>

<span data-ttu-id="80a8c-117">TYPEFLAG \_ FCONTROL、LIBFLAG \_ FCONTROL</span><span class="sxs-lookup"><span data-stu-id="80a8c-117">TYPEFLAG\_FCONTROL, LIBFLAG\_FCONTROL</span></span>

## <a name="examples"></a><span data-ttu-id="80a8c-118">範例</span><span class="sxs-lookup"><span data-stu-id="80a8c-118">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("Hello 2.1 COM Control Library"), 
    control,version(2.1)
] 
library Hello 
{ 
    /* library definitions */
}
```

## <a name="see-also"></a><span data-ttu-id="80a8c-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="80a8c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80a8c-120">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="80a8c-120">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="80a8c-121">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="80a8c-121">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="80a8c-122">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="80a8c-122">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="80a8c-123">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="80a8c-123">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="80a8c-124">**coclass**</span><span class="sxs-lookup"><span data-stu-id="80a8c-124">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="80a8c-125">**圖書館**</span><span class="sxs-lookup"><span data-stu-id="80a8c-125">**library**</span></span>](library.md)
</dt> </dl>

 

 