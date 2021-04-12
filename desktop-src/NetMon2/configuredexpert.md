---
description: CONFIGUREDEXPERT 結構會讓專家與其設定資料產生關聯。
ms.assetid: 96a6650b-6d6f-495e-83bb-385d44ff015d
title: 'CONFIGUREDEXPERT 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONFIGUREDEXPERT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3f3d40bf5d38c6b5151691a7d15bd93bef01eee5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192963"
---
# <a name="configuredexpert-structure"></a><span data-ttu-id="98e0f-103">CONFIGUREDEXPERT 結構</span><span class="sxs-lookup"><span data-stu-id="98e0f-103">CONFIGUREDEXPERT structure</span></span>

<span data-ttu-id="98e0f-104">**CONFIGUREDEXPERT** 結構會讓專家與其設定資料產生關聯。</span><span class="sxs-lookup"><span data-stu-id="98e0f-104">The **CONFIGUREDEXPERT** structure associates an expert with its configuration data.</span></span>

## <a name="syntax"></a><span data-ttu-id="98e0f-105">語法</span><span class="sxs-lookup"><span data-stu-id="98e0f-105">Syntax</span></span>


```C++
typedef struct {
  HEXPERT       hExpert;
  DWORD         StartupFlags;
  PEXPERTCONFIG pConfig;
} CONFIGUREDEXPERT, *PCONFIGUREDEXPERT;
```



## <a name="members"></a><span data-ttu-id="98e0f-106">成員</span><span class="sxs-lookup"><span data-stu-id="98e0f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="98e0f-107">**hExpert**</span><span class="sxs-lookup"><span data-stu-id="98e0f-107">**hExpert**</span></span>
</dt> <dd>

<span data-ttu-id="98e0f-108">專家的控點。</span><span class="sxs-lookup"><span data-stu-id="98e0f-108">Handle to an expert.</span></span>

</dd> <dt>

<span data-ttu-id="98e0f-109">**StartupFlags**</span><span class="sxs-lookup"><span data-stu-id="98e0f-109">**StartupFlags**</span></span>
</dt> <dd>

<span data-ttu-id="98e0f-110">專家的啟動旗標值。</span><span class="sxs-lookup"><span data-stu-id="98e0f-110">Startup flag values of the expert.</span></span>

</dd> <dt>

<span data-ttu-id="98e0f-111">**pConfig**</span><span class="sxs-lookup"><span data-stu-id="98e0f-111">**pConfig**</span></span>
</dt> <dd>

<span data-ttu-id="98e0f-112">[**EXPERTCONFIG**](expertconfig.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="98e0f-112">Pointer to an [**EXPERTCONFIG**](expertconfig.md) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="98e0f-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="98e0f-113">Requirements</span></span>



| <span data-ttu-id="98e0f-114">需求</span><span class="sxs-lookup"><span data-stu-id="98e0f-114">Requirement</span></span> | <span data-ttu-id="98e0f-115">值</span><span class="sxs-lookup"><span data-stu-id="98e0f-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="98e0f-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="98e0f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="98e0f-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="98e0f-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="98e0f-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="98e0f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="98e0f-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="98e0f-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="98e0f-120">標頭</span><span class="sxs-lookup"><span data-stu-id="98e0f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="98e0f-121"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="98e0f-121"><dt>Netmon.h</dt></span></span> </dl> |



 

 




