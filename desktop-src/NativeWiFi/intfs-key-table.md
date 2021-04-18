---
description: 包含無線設定服務所管理之所有無線區域網路介面的重要資訊表格。
ms.assetid: 5d5fe222-6ca1-4778-9f64-1c6a63467a6c
title: 'INTFS_KEY_TABLE 結構 (Wzcsapi .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTFS_KEY_TABLE
api_type:
- HeaderDef
api_location:
- Wzcsapi.h
ms.openlocfilehash: 4ef38f2317c763eaa6c7e0379be5c8b00c0ed6b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971429"
---
# <a name="intfs_key_table-structure"></a><span data-ttu-id="fd0d0-103">INTFS 索引 \_ 鍵 \_ 資料表結構</span><span class="sxs-lookup"><span data-stu-id="fd0d0-103">INTFS\_KEY\_TABLE structure</span></span>

<span data-ttu-id="fd0d0-104">\[**INTFS \_Windows \_** Vista 和 windows Server 2008 不再支援索引鍵資料表。</span><span class="sxs-lookup"><span data-stu-id="fd0d0-104">\[**INTFS\_KEY\_TABLE** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="fd0d0-105">相反地，請使用 [原生 WIFI API](native-wifi-reference.md)，它會提供類似的功能。</span><span class="sxs-lookup"><span data-stu-id="fd0d0-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="fd0d0-106">如需詳細資訊，請參閱 [關於原生 WIFI API](about-the-native-wifi-api.md)。\]</span><span class="sxs-lookup"><span data-stu-id="fd0d0-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="fd0d0-107">**INTFS 索引 \_ 鍵 \_ 資料表** 結構包含無線設定服務所管理之所有無線區域網路介面的重要資訊表格。</span><span class="sxs-lookup"><span data-stu-id="fd0d0-107">The **INTFS\_KEY\_TABLE** structure contains the table of key information for all wireless LAN interfaces managed by the Wireless Configuration Service.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd0d0-108">語法</span><span class="sxs-lookup"><span data-stu-id="fd0d0-108">Syntax</span></span>


```C++
typedef struct {
  DWORD           dwNumIntfs;
  PINTF_KEY_ENTRY pIntfs;
} INTFS_KEY_TABLE, *PINTFS_KEY_TABLE;
```



## <a name="members"></a><span data-ttu-id="fd0d0-109">成員</span><span class="sxs-lookup"><span data-stu-id="fd0d0-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="fd0d0-110">**dwNumIntfs**</span><span class="sxs-lookup"><span data-stu-id="fd0d0-110">**dwNumIntfs**</span></span>
</dt> <dd>

<span data-ttu-id="fd0d0-111">介面的總數目。</span><span class="sxs-lookup"><span data-stu-id="fd0d0-111">Total number of interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="fd0d0-112">**pIntfs**</span><span class="sxs-lookup"><span data-stu-id="fd0d0-112">**pIntfs**</span></span>
</dt> <dd>

<span data-ttu-id="fd0d0-113">[**INTF \_ \_ 索引鍵輸入**](intf-key-entry.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="fd0d0-113">Pointer to the [**INTF\_KEY\_ENTRY**](intf-key-entry.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fd0d0-114">備註</span><span class="sxs-lookup"><span data-stu-id="fd0d0-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fd0d0-115">Windows SDK 中無法使用 *Wzcsapi .h* 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="fd0d0-115">The *Wzcsapi.h* header file is not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fd0d0-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd0d0-116">Requirements</span></span>



| <span data-ttu-id="fd0d0-117">需求</span><span class="sxs-lookup"><span data-stu-id="fd0d0-117">Requirement</span></span> | <span data-ttu-id="fd0d0-118">值</span><span class="sxs-lookup"><span data-stu-id="fd0d0-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fd0d0-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fd0d0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fd0d0-120">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd0d0-120">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="fd0d0-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fd0d0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fd0d0-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd0d0-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="fd0d0-123">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="fd0d0-123">End of client support</span></span><br/>    | <span data-ttu-id="fd0d0-124">Windows XP （含 SP3）</span><span class="sxs-lookup"><span data-stu-id="fd0d0-124">Windows XP with SP3</span></span><br/>                                                       |
| <span data-ttu-id="fd0d0-125">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="fd0d0-125">End of server support</span></span><br/>    | <span data-ttu-id="fd0d0-126">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fd0d0-126">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="fd0d0-127">標頭</span><span class="sxs-lookup"><span data-stu-id="fd0d0-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd0d0-128"><dt>Wzcsapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="fd0d0-128"><dt>Wzcsapi.h</dt></span></span> </dl> |



 

 




