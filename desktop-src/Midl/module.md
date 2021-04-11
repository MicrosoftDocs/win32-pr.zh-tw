---
title: module 屬性
description: Module 語句會定義一組函數，通常是一組 DLL 進入點。
ms.assetid: 4dec207f-98bc-4784-a3c9-506ffe7523fe
keywords:
- module 屬性 MIDL
topic_type:
- apiref
api_name:
- module
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1eb310c3e126caf9b25b8c015b840aea11791d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314878"
---
# <a name="module-attribute"></a><span data-ttu-id="de882-104">module 屬性</span><span class="sxs-lookup"><span data-stu-id="de882-104">module attribute</span></span>

<span data-ttu-id="de882-105">**Module** 語句會定義一組函數，通常是一組 DLL 進入點。</span><span class="sxs-lookup"><span data-stu-id="de882-105">The **module** statement defines a group of functions, typically a set of DLL entry points.</span></span>

``` syntax
[
    attributes
]
module modulename 
{
    elementlist
};
```

## <a name="parameters"></a><span data-ttu-id="de882-106">參數</span><span class="sxs-lookup"><span data-stu-id="de882-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de882-107">*attributes*</span><span class="sxs-lookup"><span data-stu-id="de882-107">*attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="de882-108">在 \[ [](uuid.md) \] \[ [](version.md) \] module 語句之前，會接受 uuid、version、 \[ [**helpstring**](helpstring.md) \] 、 \[ [**helpcoNtext**](helpcontext.md) \] 、 \[ [**hidden**](hidden.md) \] 和 \[ [**dllname**](dllname-str-.md) \] 屬性。 </span><span class="sxs-lookup"><span data-stu-id="de882-108">The \[[**uuid**](uuid.md)\], \[[**version**](version.md)\], \[[**helpstring**](helpstring.md)\], \[[**helpcontext**](helpcontext.md)\], \[[**hidden**](hidden.md)\], and \[[**dllname**](dllname-str-.md)\] attributes are accepted before a **module** statement.</span></span> <span data-ttu-id="de882-109">如需模組定義之前所接受屬性的詳細資訊，請參閱 OLE Automation 書籍中的 [屬性描述](/previous-versions/windows/desktop/automat/attribute-descriptions)。</span><span class="sxs-lookup"><span data-stu-id="de882-109">See [Attribute Descriptions](/previous-versions/windows/desktop/automat/attribute-descriptions), in the OLE Automation book, for more information on the attributes accepted before a module definition.</span></span> <span data-ttu-id="de882-110">需要 \[ **dllname** \] 屬性。</span><span class="sxs-lookup"><span data-stu-id="de882-110">The \[**dllname**\] attribute is required.</span></span> <span data-ttu-id="de882-111">如果省略 \[ **uuid** \] 屬性，系統就不會在系統中唯一指定該模組。</span><span class="sxs-lookup"><span data-stu-id="de882-111">If the \[**uuid**\] attribute is omitted, the module is not uniquely specified in the system.</span></span>

</dd> <dt>

<span data-ttu-id="de882-112">*modulename*</span><span class="sxs-lookup"><span data-stu-id="de882-112">*modulename*</span></span> 
</dt> <dd>

<span data-ttu-id="de882-113">模組的名稱。</span><span class="sxs-lookup"><span data-stu-id="de882-113">The name of the module.</span></span>

</dd> <dt>

<span data-ttu-id="de882-114">*elementlist*</span><span class="sxs-lookup"><span data-stu-id="de882-114">*elementlist*</span></span> 
</dt> <dd>

<span data-ttu-id="de882-115">DLL 中每個函式的常數定義清單和函式原型。</span><span class="sxs-lookup"><span data-stu-id="de882-115">List of constant definitions and function prototypes for each function in the DLL.</span></span> <span data-ttu-id="de882-116">函式定義中可以出現任何數目的函式定義。</span><span class="sxs-lookup"><span data-stu-id="de882-116">Any number of function definitions can appear in the function list.</span></span> <span data-ttu-id="de882-117">函數清單中的函式具有下列形式：</span><span class="sxs-lookup"><span data-stu-id="de882-117">A function in the function list has the following form:</span></span>

<span data-ttu-id="de882-118">\[*屬性* \]*returntype* \[*呼叫慣例 funcname* \] (*參數*) ;</span><span class="sxs-lookup"><span data-stu-id="de882-118">\[*attributes*\] *returntype* \[*calling convention funcname*\](*params*);</span></span>

<span data-ttu-id="de882-119">\[*屬性* \][**const**](const.md) constanttype *constname*  =  *constval*;</span><span class="sxs-lookup"><span data-stu-id="de882-119">\[*attributes*\] [**const**](const.md) constanttype *constname* = *constval*;</span></span>

<span data-ttu-id="de882-120">Const 只 \[ 接受 [**helpstring**](helpstring.md) \] 和 \[ [**helpcoNtext**](helpcontext.md) \] 屬性。 [](const.md)</span><span class="sxs-lookup"><span data-stu-id="de882-120">Only the \[[**helpstring**](helpstring.md)\] and \[[**helpcontext**](helpcontext.md)\] attributes are accepted for a [**const**](const.md).</span></span>

<span data-ttu-id="de882-121">模組中的函式接受下列屬性： \[ [**helpstring**](helpstring.md) \] 、 \[ [**helpcoNtext**](helpcontext.md) \] 、 \[ [**string**](string.md) \] 、 \[ [**entry**](entry.md) \] 、 \[ [**propget**](propget.md) \] 、 \[ [**propput**](propput.md) \] 、 \[ [**propputref**](propputref.md) \] 和 \[ [**vararg**](vararg.md) \] 。</span><span class="sxs-lookup"><span data-stu-id="de882-121">The following attributes are accepted on a function in a module: \[[**helpstring**](helpstring.md)\], \[[**helpcontext**](helpcontext.md)\], \[[**string**](string.md)\], \[[**entry**](entry.md)\], \[[**propget**](propget.md)\], \[[**propput**](propput.md)\], \[[**propputref**](propputref.md)\], and \[[**vararg**](vararg.md)\].</span></span> <span data-ttu-id="de882-122">如果 \[ 指定了 **vararg** \] ，則最後一個參數必須是 **VARIANT** 類型的安全陣列。</span><span class="sxs-lookup"><span data-stu-id="de882-122">If \[**vararg**\] is specified, the last parameter must be a safe array of **VARIANT** type.</span></span>

<span data-ttu-id="de882-123">選擇性的呼叫慣例可以是 \_ \_ pascal/ \_ pascal/pascal、 \_ \_ cdecl/ \_ cdecl/cdecl 或 \_ \_ stdcall/ \_ stdcall/stdcall 中的一個。</span><span class="sxs-lookup"><span data-stu-id="de882-123">The optional calling convention can be one of \_\_pascal/\_pascal/pascal, \_\_cdecl/\_cdecl/cdecl, or \_\_stdcall/\_stdcall/stdcall.</span></span> <span data-ttu-id="de882-124">*呼叫慣例型別 paramname* 最多可以包含兩個前置底線。</span><span class="sxs-lookup"><span data-stu-id="de882-124">The *calling convention type paramname* can include up to two leading underscores.</span></span>

<span data-ttu-id="de882-125">參數清單是以逗號分隔的清單：</span><span class="sxs-lookup"><span data-stu-id="de882-125">The parameter list is a comma-delimited list of:</span></span>

<span data-ttu-id="de882-126">\[*屬性*\]</span><span class="sxs-lookup"><span data-stu-id="de882-126">\[*attributes*\]</span></span>

<span data-ttu-id="de882-127">此類型可以是任何先前宣告的類型或內建類型、任何類型的指標，或內建類型的指標。</span><span class="sxs-lookup"><span data-stu-id="de882-127">The type can be any previously declared type or built-in type, a pointer to any type, or a pointer to a built-in type.</span></span> <span data-ttu-id="de882-128">參數上的屬性為：</span><span class="sxs-lookup"><span data-stu-id="de882-128">Attributes on parameters are:</span></span>

<span data-ttu-id="de882-129">\[[**in**](in.md) \] 、 \[ [**out**](out-idl.md) \] 、 \[ [**optional**](optional.md) \] 。</span><span class="sxs-lookup"><span data-stu-id="de882-129">\[[**in**](in.md)\], \[[**out**](out-idl.md)\], \[[**optional**](optional.md)\].</span></span>

<span data-ttu-id="de882-130">如果 \[ 使用 [**選擇性**](optional.md) \] ，則這些參數的類型必須是 **variant** 或 **variant** \* 。</span><span class="sxs-lookup"><span data-stu-id="de882-130">If \[[**optional**](optional.md)\] is used, the types of those parameters must be **VARIANT** or **VARIANT**\*.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de882-131">備註</span><span class="sxs-lookup"><span data-stu-id="de882-131">Remarks</span></span>

<span data-ttu-id="de882-132">模組的標頭檔 ( .h) 輸出是一系列的函式原型。</span><span class="sxs-lookup"><span data-stu-id="de882-132">The header file (.h) output for modules is a series of function prototypes.</span></span> <span data-ttu-id="de882-133">**模組** 關鍵字和周圍括弧會從標頭中移除 ( .h) 檔案輸出，但是會在原型之前插入批註 (//**模組** *modulename*) 。</span><span class="sxs-lookup"><span data-stu-id="de882-133">The **module** keyword and surrounding brackets are stripped from the header (.h) file output, but a comment (// **module** *modulename*) is inserted before the prototypes.</span></span> <span data-ttu-id="de882-134">關鍵字 **extern** 會在宣告之前插入。</span><span class="sxs-lookup"><span data-stu-id="de882-134">The keyword **extern** is inserted before the declarations.</span></span>

## <a name="examples"></a><span data-ttu-id="de882-135">範例</span><span class="sxs-lookup"><span data-stu-id="de882-135">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("This is not GDI.EXE"), 
    helpcontext(190), 
    dllname("MATH.DLL")
] 
module somemodule
{ 
    [helpstring("Color for the frame")] 
            unsigned long const COLOR_FRAME = 0xH80000006; 
    [helpstring("Not a rectangle but a square"), 
     entry(1)] 
            pascal double square([in] double x); 
};
```

## <a name="see-also"></a><span data-ttu-id="de882-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="de882-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de882-137">**const**</span><span class="sxs-lookup"><span data-stu-id="de882-137">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="de882-138">型別程式庫的內容</span><span class="sxs-lookup"><span data-stu-id="de882-138">Contents of a Type Library</span></span>](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[<span data-ttu-id="de882-139">**dllname**</span><span class="sxs-lookup"><span data-stu-id="de882-139">**dllname**</span></span>](dllname-str-.md)
</dt> <dt>

[<span data-ttu-id="de882-140">**進入**</span><span class="sxs-lookup"><span data-stu-id="de882-140">**entry**</span></span>](entry.md)
</dt> <dt>

[<span data-ttu-id="de882-141">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="de882-141">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="de882-142">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="de882-142">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="de882-143">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="de882-143">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="de882-144">**隱藏**</span><span class="sxs-lookup"><span data-stu-id="de882-144">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="de882-145">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="de882-145">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="de882-146">**propget**</span><span class="sxs-lookup"><span data-stu-id="de882-146">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="de882-147">**propput**</span><span class="sxs-lookup"><span data-stu-id="de882-147">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="de882-148">**propputref**</span><span class="sxs-lookup"><span data-stu-id="de882-148">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="de882-149">**字串**</span><span class="sxs-lookup"><span data-stu-id="de882-149">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="de882-150">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="de882-150">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="de882-151">**uuid**</span><span class="sxs-lookup"><span data-stu-id="de882-151">**uuid**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="de882-152">**vararg**</span><span class="sxs-lookup"><span data-stu-id="de882-152">**vararg**</span></span>](vararg.md)
</dt> <dt>

[<span data-ttu-id="de882-153">**版本**</span><span class="sxs-lookup"><span data-stu-id="de882-153">**version**</span></span>](version.md)
</dt> </dl>

 

 