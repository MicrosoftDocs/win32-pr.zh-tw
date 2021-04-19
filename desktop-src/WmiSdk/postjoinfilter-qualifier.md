---
description: 您可以藉由將 WQL 查詢指派給 PostJoinFilter 限定詞，來篩選聯結視圖類別的實例。
ms.assetid: 926a7262-ea6b-4a5a-8aa7-6ec0ae389031
ms.tgt_platform: multiple
title: PostJoinFilter 辨識符號
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PostJoinFilter
api_type:
- NA
api_location: ''
ms.openlocfilehash: ac86aeafefc8057a1612c5007e55e7633c655c59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994407"
---
# <a name="postjoinfilter-qualifier"></a><span data-ttu-id="2ba63-103">PostJoinFilter 辨識符號</span><span class="sxs-lookup"><span data-stu-id="2ba63-103">PostJoinFilter Qualifier</span></span>

<span data-ttu-id="2ba63-104">您可以藉由將 WQL 查詢指派給 **PostJoinFilter** 限定詞，來篩選聯結視圖類別的實例。</span><span class="sxs-lookup"><span data-stu-id="2ba63-104">You can filter the instances of a join view class by assigning a WQL query to the **PostJoinFilter** qualifier.</span></span> <span data-ttu-id="2ba63-105">WQL 查詢的值會套用到聯結視圖類別的實例。</span><span class="sxs-lookup"><span data-stu-id="2ba63-105">The value of the WQL query is applied to the instances of the join view class.</span></span> <span data-ttu-id="2ba63-106">您可以使用這個辨識符號，將 view 類別的實例限制為符合特定條件的實例。</span><span class="sxs-lookup"><span data-stu-id="2ba63-106">You can use this qualifier to restrict the instances of your view class to those that meet specific conditions.</span></span> <span data-ttu-id="2ba63-107">下列 WQL 查詢會篩選依據 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)實例所呼叫之聯結類別的實例。</span><span class="sxs-lookup"><span data-stu-id="2ba63-107">The following WQL query filters instances of a join class called based on instances of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span>


```C++
PostJoinFilter("SELECT * FROM JoinDrive" +
    " WHERE FreeSpace > 1000000" +
    " and Description = \"3 1/2 Inch Floppy Drive\"")
```



<span data-ttu-id="2ba63-108">使用此辨識符號有數項限制：</span><span class="sxs-lookup"><span data-stu-id="2ba63-108">There are several restrictions to the use of this qualifier:</span></span>

-   <span data-ttu-id="2ba63-109">**PostJoinFilter** 僅適用于聯結視圖類別。</span><span class="sxs-lookup"><span data-stu-id="2ba63-109">**PostJoinFilter** is only available to join view classes.</span></span>
-   <span data-ttu-id="2ba63-110">查詢中指定的類別名稱和屬性名稱會參考 view 類別的屬性，而非來源類別的屬性。</span><span class="sxs-lookup"><span data-stu-id="2ba63-110">The class name and property names specified in the query refer to the properties of the view class, not the source class.</span></span>
-   <span data-ttu-id="2ba63-111">不允許排除屬性;只 `SELECT *` 允許型別查詢。</span><span class="sxs-lookup"><span data-stu-id="2ba63-111">No exclusion of properties is permitted; only `SELECT *` type queries are allowed.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ba63-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ba63-112">Requirements</span></span>



| <span data-ttu-id="2ba63-113">需求</span><span class="sxs-lookup"><span data-stu-id="2ba63-113">Requirement</span></span> | <span data-ttu-id="2ba63-114">值</span><span class="sxs-lookup"><span data-stu-id="2ba63-114">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="2ba63-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2ba63-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2ba63-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2ba63-116">Windows Vista</span></span><br/>       |
| <span data-ttu-id="2ba63-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2ba63-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2ba63-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ba63-118">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2ba63-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ba63-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ba63-120">**視圖提供者專用的限定詞**</span><span class="sxs-lookup"><span data-stu-id="2ba63-120">**Qualifiers Specific to the View Provider**</span></span>](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

