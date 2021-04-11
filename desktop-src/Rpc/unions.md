---
title: 'union 關鍵字 (RPC) '
description: 等位需要特殊的 MIDL 關鍵字，以支援其與遠端程序呼叫 (RPC) 的使用。
ms.assetid: e7c8296c-893d-4df7-913a-f969733e1917
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c562815d78ab931bd4d6590b5465647e72f4bf6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315241"
---
# <a name="union-keyword-rpc"></a><span data-ttu-id="c8af3-103">union 關鍵字 (RPC) </span><span class="sxs-lookup"><span data-stu-id="c8af3-103">union keyword (RPC)</span></span>

<span data-ttu-id="c8af3-104">C 語言的某些功能（例如等位）需要特殊的 MIDL 關鍵字，才能支援在遠端程序呼叫中使用。</span><span class="sxs-lookup"><span data-stu-id="c8af3-104">Some features of the C language, such as unions, require special MIDL keywords to support their use in remote procedure calls.</span></span> <span data-ttu-id="c8af3-105">C 語言中的等位是一個變數，可保存不同類型和大小的物件。</span><span class="sxs-lookup"><span data-stu-id="c8af3-105">A union in the C language is a variable that holds objects of different types and sizes.</span></span> <span data-ttu-id="c8af3-106">開發人員通常會建立一個變數，以追蹤儲存在等位中的類型。</span><span class="sxs-lookup"><span data-stu-id="c8af3-106">The developer usually creates a variable to keep track of the types stored in the union.</span></span> <span data-ttu-id="c8af3-107">若要在分散式環境中正確運作，表示聯集類型或 *判別* 的變數也必須可供遠端電腦使用。</span><span class="sxs-lookup"><span data-stu-id="c8af3-107">To operate correctly in a distributed environment, the variable that indicates the type of the union, or the *discriminant*, must also be available to the remote computer.</span></span> <span data-ttu-id="c8af3-108">MIDL 提供 \[ [**switch \_ 型**](/windows/desktop/Midl/switch-type)別 \] ，而 \[ [**參數 \_ 則是**](/windows/desktop/Midl/switch-is)用 \] 來識別判別型別和名稱的關鍵字。</span><span class="sxs-lookup"><span data-stu-id="c8af3-108">MIDL provides the \[[**switch\_type**](/windows/desktop/Midl/switch-type)\] and \[[**switch\_is**](/windows/desktop/Midl/switch-is)\] keywords to identify the discriminant type and name.</span></span>

<span data-ttu-id="c8af3-109">MIDL 需要以兩種方式之一，以聯集傳輸判別：</span><span class="sxs-lookup"><span data-stu-id="c8af3-109">MIDL requires that the discriminant be transmitted with the union in one of two ways:</span></span>

-   <span data-ttu-id="c8af3-110">Union 和判別必須提供為參數。</span><span class="sxs-lookup"><span data-stu-id="c8af3-110">The union and the discriminant must be provided as parameters.</span></span>
-   <span data-ttu-id="c8af3-111">Union 和判別必須封裝在結構中。</span><span class="sxs-lookup"><span data-stu-id="c8af3-111">The union and the discriminant must be packaged in a structure.</span></span>

<span data-ttu-id="c8af3-112">MIDL： [**nonencapsulated \_ union**](/windows/desktop/Midl/nonencapsulated-unions) 和 [**封裝聯 \_ 集**](/windows/desktop/Midl/encapsulated-unions)提供兩種基本類型的區分等位。</span><span class="sxs-lookup"><span data-stu-id="c8af3-112">Two fundamental types of discriminated unions are provided by MIDL: [**nonencapsulated\_union**](/windows/desktop/Midl/nonencapsulated-unions) and [**encapsulated\_union**](/windows/desktop/Midl/encapsulated-unions).</span></span> <span data-ttu-id="c8af3-113">如果聯集是參數，nonencapsulated 聯集的判別就是另一個參數。</span><span class="sxs-lookup"><span data-stu-id="c8af3-113">The discriminant of a nonencapsulated union is another parameter if the union is a parameter.</span></span> <span data-ttu-id="c8af3-114">如果等位是結構的欄位，則它是另一個欄位。</span><span class="sxs-lookup"><span data-stu-id="c8af3-114">It is another field if the union is a field of a structure.</span></span> <span data-ttu-id="c8af3-115">封裝聯集的定義會轉換成結構定義，其第一個欄位為判別，而第二個和最後一個欄位為聯集。</span><span class="sxs-lookup"><span data-stu-id="c8af3-115">The definition of an encapsulated union is turned into a structure definition whose first field is the discriminant and whose second and last fields are the union.</span></span> <span data-ttu-id="c8af3-116">下列範例示範如何提供 union 和判別作為參數：</span><span class="sxs-lookup"><span data-stu-id="c8af3-116">The following example demonstrates how to provide the union and discriminant as parameters:</span></span>

``` syntax
typedef [switch_type(short)] union 
{
    [case(0)]    short     sVal;
    [case(1)]    float     fVal;
    [case(2)]    char      chVal;
    [default]    ;
} DISCRIM_UNION_PARAM_TYPE;
 
short UnionParamProc(
    [in, switch_is(sUtype)] DISCRIM_UNION_PARAM_TYPE Union,
    [in] short sUtype);
```

<span data-ttu-id="c8af3-117">上述範例中的聯集可以包含單一值： **short**、 **float** 或 **char**。</span><span class="sxs-lookup"><span data-stu-id="c8af3-117">The union in the preceding example can contain a single value: either **short**, **float**, or **char**.</span></span> <span data-ttu-id="c8af3-118">Union 的型別定義包含 MIDL **switch \_ type** 屬性（attribute），此屬性（attribute）會指定判別的型別。</span><span class="sxs-lookup"><span data-stu-id="c8af3-118">The type definition for the union includes the MIDL **switch\_type** attribute that specifies the type of the discriminant.</span></span> <span data-ttu-id="c8af3-119">在這裡， \[ switch \_ 類型 (short) \] 指定判別的類型為 **short**。</span><span class="sxs-lookup"><span data-stu-id="c8af3-119">Here, \[switch\_type(short)\] specifies that the discriminant is of type **short**.</span></span> <span data-ttu-id="c8af3-120">參數必須是整數類型。</span><span class="sxs-lookup"><span data-stu-id="c8af3-120">The switch must be an integer type.</span></span>

<span data-ttu-id="c8af3-121">如果聯集是結構的成員，則判別必須是相同結構的成員。</span><span class="sxs-lookup"><span data-stu-id="c8af3-121">If the union is a member of a structure, then the discriminant must be a member of the same structure.</span></span> <span data-ttu-id="c8af3-122">如果 union 是參數，則判別必須是另一個參數。</span><span class="sxs-lookup"><span data-stu-id="c8af3-122">If the union is a parameter, then the discriminant must be another parameter.</span></span> <span data-ttu-id="c8af3-123">在上述範例中， **UnionParamProc** 函式的原型會將判別 *sUtype* 顯示為呼叫的最後一個參數。</span><span class="sxs-lookup"><span data-stu-id="c8af3-123">The prototype for the function **UnionParamProc** in the preceding example shows the discriminant *sUtype* as the last parameter of the call.</span></span> <span data-ttu-id="c8af3-124"> (判別可以出現在呼叫中的任何位置。 ) 參數中指定的參數類型 **\[ \_ ，就 \]** 必須符合 **\[ switch \_ type \]** 屬性中指定的型別。</span><span class="sxs-lookup"><span data-stu-id="c8af3-124">(The discriminant can appear in any position in the call.) The type of the parameter specified in the **\[switch\_is\]** attribute must match the type specified in the **\[switch\_type\]** attribute.</span></span>

<span data-ttu-id="c8af3-125">下列範例示範如何使用封裝判別與聯集的單一結構：</span><span class="sxs-lookup"><span data-stu-id="c8af3-125">The following example demonstrates the use of a single structure that packages the discriminant with the union:</span></span>

``` syntax
typedef struct 
{
    short utype;  /* discriminant can precede or follow union */
    [switch_is(utype)] union 
    {
       [case(0)]   short     sVal;
       [case(1)]   float     fVal;
       [case(2)]   char      chVal;
       [default]   ;
    } u;
} DISCRIM_UNION_STRUCT_TYPE;
 
short UnionStructProc(
    [in] DISCRIM_UNION_STRUCT_TYPE u1);
```

<span data-ttu-id="c8af3-126">Microsoft RPC MIDL 編譯器允許在 [**typedef**](/windows/desktop/Midl/typedef) 結構之外進行聯集宣告。</span><span class="sxs-lookup"><span data-stu-id="c8af3-126">The Microsoft RPC MIDL compiler allows union declarations outside of [**typedef**](/windows/desktop/Midl/typedef) constructs.</span></span> <span data-ttu-id="c8af3-127">這項功能是 DCE IDL 的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="c8af3-127">This feature is an extension to DCE IDL.</span></span> <span data-ttu-id="c8af3-128">如需詳細資訊，請參閱聯 [**集**](/windows/desktop/Midl/union)。</span><span class="sxs-lookup"><span data-stu-id="c8af3-128">For more information, see [**union**](/windows/desktop/Midl/union).</span></span>

 

 