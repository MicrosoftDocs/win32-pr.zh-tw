---
title: v1_enum 屬性
description: '\ V1 \_ enum \ 屬性會指示指定的列舉型別以32位實體（而非16位預設值）傳輸。'
ms.assetid: 46016131-b78e-4a7f-94c8-41ff1780b0b8
keywords:
- v1_enum 屬性 MIDL
topic_type:
- apiref
api_name:
- v1_enum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8183b8b91c4a061e6b91c67ab83bca6393751f4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841323"
---
# <a name="v1_enum-attribute"></a><span data-ttu-id="ac47b-104">v1 \_ 列舉屬性</span><span class="sxs-lookup"><span data-stu-id="ac47b-104">v1\_enum attribute</span></span>

<span data-ttu-id="ac47b-105">**\[ V1 \_ 列舉 \]** 屬性會指示指定的列舉型別以32位實體的形式傳送，而不是16位的預設值。</span><span class="sxs-lookup"><span data-stu-id="ac47b-105">The **\[v1\_enum\]** attribute directs that the specified enumerated type be transmitted as a 32-bit entity, rather than the 16-bit default.</span></span>

``` syntax
[v1_enum] enum 
{
    ...
};
```

## <a name="parameters"></a><span data-ttu-id="ac47b-106">參數</span><span class="sxs-lookup"><span data-stu-id="ac47b-106">Parameters</span></span>

<span data-ttu-id="ac47b-107">這個屬性沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="ac47b-107">This attribute has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac47b-108">備註</span><span class="sxs-lookup"><span data-stu-id="ac47b-108">Remarks</span></span>

<span data-ttu-id="ac47b-109">使用 **\[ v1 \_ enum \]** 屬性將列舉型別傳輸為32位實體，可提高在結構或等位中內嵌這類列舉時，封送處理和封送處理資料的效率。</span><span class="sxs-lookup"><span data-stu-id="ac47b-109">Using the **\[v1\_enum\]** attribute to transmit an enumerated type as a 32-bit entity increases the efficiency of marshaling and unmarshaling data when such an enumeration is embedded in structures or unions.</span></span>

<span data-ttu-id="ac47b-110">為了改善效能，建議您將 **\[ v1 \_ 列舉 \]** 屬性套用至32位應用程式中的枚舉器。</span><span class="sxs-lookup"><span data-stu-id="ac47b-110">For improved performance, we recommend applying the **\[v1\_enum\]** attribute to enumerators in 32-bit applications.</span></span> <span data-ttu-id="ac47b-111">不過請記住，在16位平臺上，C 編譯器會將列舉型別視為16位 [**整數**](int.md)。因此，16位用戶端應用程式需要將 [**列舉**](enum.md) 類型轉換為 [**long**](long.md) 以進行遠端傳輸，以避免覆寫資料或傳送不正確的值。</span><span class="sxs-lookup"><span data-stu-id="ac47b-111">Keep in mind, however, that on 16-bit platforms the C compiler treats an enumerated type as a 16-bit [**int**](int.md). Therefore 16-bit client applications need to convert [**enum**](enum.md) types to [**long**](long.md) for remote transmission in order to avoid overwriting data or sending incorrect values.</span></span>

## <a name="examples"></a><span data-ttu-id="ac47b-112">範例</span><span class="sxs-lookup"><span data-stu-id="ac47b-112">Examples</span></span>

``` syntax
typedef [v1_enum] enum 
{
    value1, 
    value2, ...
};
```

## <a name="see-also"></a><span data-ttu-id="ac47b-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac47b-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac47b-114">**枚舉**</span><span class="sxs-lookup"><span data-stu-id="ac47b-114">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="ac47b-115"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="ac47b-115">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="ac47b-116">**long**</span><span class="sxs-lookup"><span data-stu-id="ac47b-116">**long**</span></span>](long.md)
</dt> </dl>

 

 




