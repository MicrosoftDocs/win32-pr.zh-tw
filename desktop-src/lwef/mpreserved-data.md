---
title: 'MPRESERVED_DATA 結構 (MpClient .h) '
description: 保留的通知資料。
ms.assetid: C92206BD-6E56-4B7D-ABB1-DC1149AE141D
keywords:
- MPRESERVED_DATA 結構舊版 Windows 環境功能
- PMPRESERVED_DATA 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPRESERVED_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b1e08184da71fe857cb412ef986c986a0c59baa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104549"
---
# <a name="mpreserved_data-structure"></a><span data-ttu-id="ca02f-105">MPRESERVED \_ 資料結構</span><span class="sxs-lookup"><span data-stu-id="ca02f-105">MPRESERVED\_DATA structure</span></span>

<span data-ttu-id="ca02f-106">保留的通知資料。</span><span class="sxs-lookup"><span data-stu-id="ca02f-106">Reserved notification data.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca02f-107">語法</span><span class="sxs-lookup"><span data-stu-id="ca02f-107">Syntax</span></span>


```C++
typedef struct tagMPRESERVED_DATA {
  DWORD cbReservedData;
  BYTE  *pbReservedData;
} MPRESERVED_DATA, *PMPRESERVED_DATA;
```



## <a name="members"></a><span data-ttu-id="ca02f-108">成員</span><span class="sxs-lookup"><span data-stu-id="ca02f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ca02f-109">**cbReservedData**</span><span class="sxs-lookup"><span data-stu-id="ca02f-109">**cbReservedData**</span></span>
</dt> <dd>

<span data-ttu-id="ca02f-110">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="ca02f-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="ca02f-111">保留資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ca02f-111">Size of reserved data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ca02f-112">**pbReservedData**</span><span class="sxs-lookup"><span data-stu-id="ca02f-112">**pbReservedData**</span></span>
</dt> <dd>

<span data-ttu-id="ca02f-113">類型：**位元組 \***</span><span class="sxs-lookup"><span data-stu-id="ca02f-113">Type: **BYTE\***</span></span>

</dd> <dd>

<span data-ttu-id="ca02f-114">保留資料的指標。</span><span class="sxs-lookup"><span data-stu-id="ca02f-114">Pointer to reserved data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ca02f-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="ca02f-115">Requirements</span></span>



| <span data-ttu-id="ca02f-116">需求</span><span class="sxs-lookup"><span data-stu-id="ca02f-116">Requirement</span></span> | <span data-ttu-id="ca02f-117">值</span><span class="sxs-lookup"><span data-stu-id="ca02f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca02f-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ca02f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ca02f-119">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ca02f-119">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ca02f-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ca02f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ca02f-121">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ca02f-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ca02f-122">標頭</span><span class="sxs-lookup"><span data-stu-id="ca02f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca02f-123"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="ca02f-123"><dt>MpClient.h</dt></span></span> </dl> |



 

 





