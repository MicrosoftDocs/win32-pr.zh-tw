---
description: 要在資料庫中存取之索引的識別碼。
ms.assetid: 559e73bf-91c2-4dbf-a667-e5c0431aaffa
title: INDEXID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b6ef6b79dd19183f575930e9793a6ab2f1f5cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111137"
---
# <a name="indexid"></a><span data-ttu-id="8f8eb-103">INDEXID</span><span class="sxs-lookup"><span data-stu-id="8f8eb-103">INDEXID</span></span>

<span data-ttu-id="8f8eb-104">要在資料庫中存取之索引的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8f8eb-104">The identifier of the index to be accessed in a database.</span></span>


```C++
typedef DWORD INDEXID;
```



## <a name="remarks"></a><span data-ttu-id="8f8eb-105">備註</span><span class="sxs-lookup"><span data-stu-id="8f8eb-105">Remarks</span></span>

<span data-ttu-id="8f8eb-106">**INDEXID** 可以是代表索引的整數值，也可以是下列值：</span><span class="sxs-lookup"><span data-stu-id="8f8eb-106">An **INDEXID** can be an integer value that represents the index, or the following value:</span></span>

<dl> <dt>

<span data-ttu-id="8f8eb-107"><span id="INDEXID_NULL___INDEXID_-1_"></span><span id="indexid_null___indexid_-1_"></span>INDEXID \_ Null ( (INDEXID) -1) </span><span class="sxs-lookup"><span data-stu-id="8f8eb-107"><span id="INDEXID_NULL___INDEXID_-1_"></span><span id="indexid_null___indexid_-1_"></span>INDEXID\_NULL ((INDEXID)-1)</span></span>
</dt> <dd>

<span data-ttu-id="8f8eb-108">不正確 **INDEXID**。</span><span class="sxs-lookup"><span data-stu-id="8f8eb-108">An invalid **INDEXID**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8f8eb-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f8eb-109">Requirements</span></span>



| <span data-ttu-id="8f8eb-110">需求</span><span class="sxs-lookup"><span data-stu-id="8f8eb-110">Requirement</span></span> | <span data-ttu-id="8f8eb-111">值</span><span class="sxs-lookup"><span data-stu-id="8f8eb-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8f8eb-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8f8eb-112">Minimum supported client</span></span><br/> | <span data-ttu-id="8f8eb-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f8eb-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8f8eb-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8f8eb-114">Minimum supported server</span></span><br/> | <span data-ttu-id="8f8eb-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f8eb-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8f8eb-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f8eb-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f8eb-117">**SdbDeclareIndex**</span><span class="sxs-lookup"><span data-stu-id="8f8eb-117">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
</dt> <dt>

[<span data-ttu-id="8f8eb-118">**SdbStartIndexing**</span><span class="sxs-lookup"><span data-stu-id="8f8eb-118">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
</dt> <dt>

[<span data-ttu-id="8f8eb-119">**SdbStopIndexing**</span><span class="sxs-lookup"><span data-stu-id="8f8eb-119">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
</dt> </dl>

 

 




