---
description: 受保護儲存方法的資料類型。
ms.assetid: 4d494326-6d0f-4a12-83a2-3c3dd3ca9c1b
title: 'PStore 類型 (Pstore) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f1c93af4ae6756a6489b828c50bac505241bdd3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977525"
---
# <a name="pstore-types"></a><span data-ttu-id="ade08-103">PStore 類型</span><span class="sxs-lookup"><span data-stu-id="ade08-103">PStore Types</span></span>

<span data-ttu-id="ade08-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="ade08-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="ade08-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="ade08-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="ade08-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="ade08-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="ade08-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="ade08-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="ade08-108">受保護儲存方法的資料類型。</span><span class="sxs-lookup"><span data-stu-id="ade08-108">The data types for Protected Storage methods.</span></span>


```C++
typedef DWORD PST_ACCESSMODE;
typedef DWORD PST_ACCESSCLAUSETYPE;
typedef DWORD PST_KEY;
```



<dl> <dt>

<span data-ttu-id="ade08-109">**PST \_ ACCESSMODE**</span><span class="sxs-lookup"><span data-stu-id="ade08-109">**PST\_ACCESSMODE**</span></span>
</dt> <dd>

<span data-ttu-id="ade08-110">定義存取規則的讀取或寫入模式。</span><span class="sxs-lookup"><span data-stu-id="ade08-110">Defines the read or write mode of the access rule.</span></span>

</dd> <dt>

<span data-ttu-id="ade08-111">**PST \_ ACCESSCLAUSETYPE**</span><span class="sxs-lookup"><span data-stu-id="ade08-111">**PST\_ACCESSCLAUSETYPE**</span></span>
</dt> <dd>

<span data-ttu-id="ade08-112">定義存取規則的子句類型。</span><span class="sxs-lookup"><span data-stu-id="ade08-112">Defines the clause type of the access rule.</span></span>

</dd> <dt>

<span data-ttu-id="ade08-113">**PST \_ 金鑰**</span><span class="sxs-lookup"><span data-stu-id="ade08-113">**PST\_KEY**</span></span>
</dt> <dd>

<span data-ttu-id="ade08-114">定義預存專案的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="ade08-114">Defines the key for the stored item.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ade08-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="ade08-115">Requirements</span></span>



| <span data-ttu-id="ade08-116">需求</span><span class="sxs-lookup"><span data-stu-id="ade08-116">Requirement</span></span> | <span data-ttu-id="ade08-117">值</span><span class="sxs-lookup"><span data-stu-id="ade08-117">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ade08-118">標頭</span><span class="sxs-lookup"><span data-stu-id="ade08-118">Header</span></span><br/> | <dl> <span data-ttu-id="ade08-119"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="ade08-119"><dt>Pstore.h</dt></span></span> </dl> |



 

 
