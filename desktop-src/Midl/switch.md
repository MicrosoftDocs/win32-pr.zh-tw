---
title: 切換屬性
description: Switch 關鍵字會選取封裝聯集的判別 \_ 。
ms.assetid: 66179b68-852f-4943-9105-e9fb310f3c2e
keywords:
- 切換屬性 MIDL
topic_type:
- apiref
api_name:
- switch
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cdf9342789d5603a3b64d778bd60364eebde50e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103932719"
---
# <a name="switch-attribute"></a><span data-ttu-id="98062-104">切換屬性</span><span class="sxs-lookup"><span data-stu-id="98062-104">switch attribute</span></span>

<span data-ttu-id="98062-105">**Switch** 關鍵字會選取 [**封裝聯 \_ 集**](encapsulated-unions.md)的判別。</span><span class="sxs-lookup"><span data-stu-id="98062-105">The **switch** keyword selects the discriminant for an [**encapsulated\_union**](encapsulated-unions.md).</span></span>

``` syntax
switch (switch-type switch-name)
```

## <a name="parameters"></a><span data-ttu-id="98062-106">參數</span><span class="sxs-lookup"><span data-stu-id="98062-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98062-107">*切換類型*</span><span class="sxs-lookup"><span data-stu-id="98062-107">*switch-type*</span></span> 
</dt> <dd>

<span data-ttu-id="98062-108">指定 [**int**](int.md)、 [**char**](-char.md)、 [**列舉**](enum.md) 型別或解析成其中一種類型的識別碼。</span><span class="sxs-lookup"><span data-stu-id="98062-108">Specifies an [**int**](int.md), [**char**](-char.md), [**enum**](enum.md) type, or an identifier that resolves to one of these types.</span></span>

</dd> <dt>

<span data-ttu-id="98062-109">*參數名稱*</span><span class="sxs-lookup"><span data-stu-id="98062-109">*switch-name*</span></span> 
</dt> <dd>

<span data-ttu-id="98062-110">指定作為聯集判別之類型 *參數* 類型的變數名稱。</span><span class="sxs-lookup"><span data-stu-id="98062-110">Specifies the name of the variable of type *switch-type* that acts as the union discriminant.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="98062-111">範例</span><span class="sxs-lookup"><span data-stu-id="98062-111">Examples</span></span>

``` syntax
typedef union _S1_TYPE switch (long l1) U1_TYPE 
{ 
    case 1024: 
        float f1; 
    case 2048: 
        double d2; 
} S1_TYPE; 
 
/* in generated header file */ 
typedef struct _S1_TYPE 
{ 
    long l1; 
    union 
    { 
        float f1; 
        double d2; 
    } U1_TYPE; 
} S1_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="98062-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="98062-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98062-113"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="98062-113">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="98062-114">Nonencapsulated 聯集</span><span class="sxs-lookup"><span data-stu-id="98062-114">Nonencapsulated Unions</span></span>](nonencapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="98062-115">**切換 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="98062-115">**switch\_is**</span></span>](switch-is.md)
</dt> <dt>

[<span data-ttu-id="98062-116">**切換 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="98062-116">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="98062-117">**聯盟**</span><span class="sxs-lookup"><span data-stu-id="98062-117">**union**</span></span>](union.md)
</dt> </dl>

 

 




