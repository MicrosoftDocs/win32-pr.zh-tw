---
description: PROTOCOLTABLE 結構包含通訊協定清單。
ms.assetid: dad2b228-5916-44fe-b78e-ebc6507dc555
title: 'PROTOCOLTABLE 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROTOCOLTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3ad79beca7ce79611747a02704ffc05da5fc3d4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983796"
---
# <a name="protocoltable-structure"></a><span data-ttu-id="e6e74-103">PROTOCOLTABLE 結構</span><span class="sxs-lookup"><span data-stu-id="e6e74-103">PROTOCOLTABLE structure</span></span>

<span data-ttu-id="e6e74-104">**PROTOCOLTABLE** 結構包含通訊協定清單。</span><span class="sxs-lookup"><span data-stu-id="e6e74-104">The **PROTOCOLTABLE** structure contains a list of protocols.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6e74-105">語法</span><span class="sxs-lookup"><span data-stu-id="e6e74-105">Syntax</span></span>


```C++
typedef struct _PROTOCOLTABLE {
  DWORD     nProtocols;
  HPROTOCOL hProtocol[1];
} PROTOCOLTABLE;
```



## <a name="members"></a><span data-ttu-id="e6e74-106">成員</span><span class="sxs-lookup"><span data-stu-id="e6e74-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e6e74-107">**nProtocols**</span><span class="sxs-lookup"><span data-stu-id="e6e74-107">**nProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="e6e74-108">已啟用的通訊協定數目。</span><span class="sxs-lookup"><span data-stu-id="e6e74-108">Number of protocols that are enabled.</span></span>

</dd> <dt>

<span data-ttu-id="e6e74-109">**hProtocol**</span><span class="sxs-lookup"><span data-stu-id="e6e74-109">**hProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="e6e74-110">啟用的通訊協定之控制碼的陣列。</span><span class="sxs-lookup"><span data-stu-id="e6e74-110">Array of handles to enabled protocols.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e6e74-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6e74-111">Requirements</span></span>



| <span data-ttu-id="e6e74-112">需求</span><span class="sxs-lookup"><span data-stu-id="e6e74-112">Requirement</span></span> | <span data-ttu-id="e6e74-113">值</span><span class="sxs-lookup"><span data-stu-id="e6e74-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e6e74-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e6e74-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e6e74-115">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6e74-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e6e74-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e6e74-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e6e74-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6e74-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e6e74-118">標頭</span><span class="sxs-lookup"><span data-stu-id="e6e74-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6e74-119"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="e6e74-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




