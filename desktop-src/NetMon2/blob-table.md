---
description: 包含 Blob 的陣列。
ms.assetid: e87f493b-f160-4316-b369-75d20c735213
title: 'BLOB_TABLE 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BLOB_TABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 32bacc925381f1c7ed30aa66247671b67e31b7e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192637"
---
# <a name="blob_table-structure"></a><span data-ttu-id="7b8c3-103">BLOB \_ 資料表結構</span><span class="sxs-lookup"><span data-stu-id="7b8c3-103">BLOB\_TABLE structure</span></span>

<span data-ttu-id="7b8c3-104">**Blob \_ 資料表** 結構包含 blob 的陣列。</span><span class="sxs-lookup"><span data-stu-id="7b8c3-104">The **BLOB\_TABLE** structure contains an array of BLOBs.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b8c3-105">語法</span><span class="sxs-lookup"><span data-stu-id="7b8c3-105">Syntax</span></span>


```C++
typedef struct {
  DWORD dwNumBlobs;
  HBLOB hBlobs[];
} BLOB_TABLE, *PBLOB_TABLE;
```



## <a name="members"></a><span data-ttu-id="7b8c3-106">成員</span><span class="sxs-lookup"><span data-stu-id="7b8c3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7b8c3-107">**dwNumBlobs**</span><span class="sxs-lookup"><span data-stu-id="7b8c3-107">**dwNumBlobs**</span></span>
</dt> <dd>

<span data-ttu-id="7b8c3-108">許多 Blob 之後的指標。</span><span class="sxs-lookup"><span data-stu-id="7b8c3-108">Indicator that many BLOBs follow.</span></span>

</dd> <dt>

<span data-ttu-id="7b8c3-109">**hBlobs**</span><span class="sxs-lookup"><span data-stu-id="7b8c3-109">**hBlobs**</span></span>
</dt> <dd>

<span data-ttu-id="7b8c3-110">BLOB 陣列的控制碼。</span><span class="sxs-lookup"><span data-stu-id="7b8c3-110">Handle to the BLOB array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b8c3-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b8c3-111">Requirements</span></span>



| <span data-ttu-id="7b8c3-112">需求</span><span class="sxs-lookup"><span data-stu-id="7b8c3-112">Requirement</span></span> | <span data-ttu-id="7b8c3-113">值</span><span class="sxs-lookup"><span data-stu-id="7b8c3-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7b8c3-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7b8c3-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7b8c3-115">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7b8c3-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7b8c3-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7b8c3-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7b8c3-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7b8c3-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7b8c3-118">標頭</span><span class="sxs-lookup"><span data-stu-id="7b8c3-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b8c3-119"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="7b8c3-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




