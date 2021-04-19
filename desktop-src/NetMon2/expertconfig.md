---
description: EXPERTCONFIG 結構包含專家的設定資料。 專家將 RawConfigData 成員與專家特定的結構重迭。
ms.assetid: 6167e846-d58c-40a8-94f7-c6d6185ae724
title: 'EXPERTCONFIG 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTCONFIG
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 293bdf4c792c10232564a7ba6386df430e81ecb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972173"
---
# <a name="expertconfig-structure"></a><span data-ttu-id="f4c98-104">EXPERTCONFIG 結構</span><span class="sxs-lookup"><span data-stu-id="f4c98-104">EXPERTCONFIG structure</span></span>

<span data-ttu-id="f4c98-105">**EXPERTCONFIG** 結構包含專家的設定資料。</span><span class="sxs-lookup"><span data-stu-id="f4c98-105">The **EXPERTCONFIG** structure contains the configuration data of the expert.</span></span> <span data-ttu-id="f4c98-106">專家將 **RawConfigData** 成員與專家特定的結構重迭。</span><span class="sxs-lookup"><span data-stu-id="f4c98-106">The expert overlays the **RawConfigData** member with an expert-specific structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4c98-107">語法</span><span class="sxs-lookup"><span data-stu-id="f4c98-107">Syntax</span></span>


```C++
typedef struct {
  DWORD RawConfigLength;
  BYTE  RawConfigData[];
} EXPERTCONFIG, *PEXPERTCONFIG;
```



## <a name="members"></a><span data-ttu-id="f4c98-108">成員</span><span class="sxs-lookup"><span data-stu-id="f4c98-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f4c98-109">**RawConfigLength**</span><span class="sxs-lookup"><span data-stu-id="f4c98-109">**RawConfigLength**</span></span>
</dt> <dd>

<span data-ttu-id="f4c98-110">結構的總長度，包括用於成員的四個位元組。</span><span class="sxs-lookup"><span data-stu-id="f4c98-110">Total length of the structure, including the four bytes used for the member.</span></span> <span data-ttu-id="f4c98-111">當結構儲存至磁片磁碟機並從磁片磁碟機讀取時，網路監視器會使用此值。</span><span class="sxs-lookup"><span data-stu-id="f4c98-111">Network Monitor uses the value when the structure is saved-to and read-from a disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="f4c98-112">**RawConfigData**</span><span class="sxs-lookup"><span data-stu-id="f4c98-112">**RawConfigData**</span></span>
</dt> <dd>

<span data-ttu-id="f4c98-113">設定資料。</span><span class="sxs-lookup"><span data-stu-id="f4c98-113">Configuration data.</span></span> <span data-ttu-id="f4c98-114">專家必須加入設定資料。</span><span class="sxs-lookup"><span data-stu-id="f4c98-114">The expert must add the configuration data.</span></span> <span data-ttu-id="f4c98-115">例如，假設您有一個看起來像這樣的資料結構。</span><span class="sxs-lookup"><span data-stu-id="f4c98-115">For example, suppose that you had a data structure that looked like this.</span></span>

``` syntax
typedef struct
{
    DWORD       RawConfigLength;   // Overlay of structure
    DWORD       PickNumEvents;
    DWORD       NumEventsSpecific;
    DWORD       PickSpeedThroughCapture;
    DWORD       PickStartup;
    DWORD       PickAttachProperties;
} TESTEXPERTCONFIG;
typedef TESTEXPERTCONFIG* LPTESTEXPERTCONFIG;
```

<span data-ttu-id="f4c98-116">請注意， **RawConfigLength** 可確保重迭的運作正常。</span><span class="sxs-lookup"><span data-stu-id="f4c98-116">Note that **RawConfigLength** ensures that the overlay works correctly.</span></span> <span data-ttu-id="f4c98-117">當您使用資料時，您的程式碼可能如下所示：</span><span class="sxs-lookup"><span data-stu-id="f4c98-117">When you use the data, your code might look like this:</span></span>

``` syntax
BOOL WINAPI Configure( 
    HEXPERTKEY ExpertKey,
    PEXPERTCONFIG * ppConfig,
    PEXPERTSTARTUPINFO pStartupInfo,
    DWORD StartupFlags,
    HWND hWnd
)
{
    LPTESTEXPERTCONFIG  lpConfig;

    //...
    lpConfig = (LPTESTEXPERTCONFIG)(*ppConfig);
    //...
}
```

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f4c98-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4c98-118">Requirements</span></span>



| <span data-ttu-id="f4c98-119">需求</span><span class="sxs-lookup"><span data-stu-id="f4c98-119">Requirement</span></span> | <span data-ttu-id="f4c98-120">值</span><span class="sxs-lookup"><span data-stu-id="f4c98-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f4c98-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f4c98-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f4c98-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4c98-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f4c98-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f4c98-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f4c98-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4c98-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f4c98-125">標頭</span><span class="sxs-lookup"><span data-stu-id="f4c98-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4c98-126"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="f4c98-126"><dt>Netmon.h</dt></span></span> </dl> |



 

 




