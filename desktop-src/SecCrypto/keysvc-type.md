---
description: KEYSVC \_ 型別列舉會定義金鑰是否適用于電腦或服務。
ms.assetid: 573a412a-1e9d-47ac-bd09-2319d4b9712b
title: 'KEYSVC_TYPE 列舉 (Rkeysvcc .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_TYPE
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 71d6724f7bae78a3c1ac4da83289c151b7ec1a73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945400"
---
# <a name="keysvc_type-enumeration"></a><span data-ttu-id="0e2ad-103">KEYSVC \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="0e2ad-103">KEYSVC\_TYPE enumeration</span></span>

<span data-ttu-id="0e2ad-104">**KEYSVC \_ 型** 別列舉會定義金鑰是否適用于電腦或服務。</span><span class="sxs-lookup"><span data-stu-id="0e2ad-104">The **KEYSVC\_TYPE** enumeration defines whether a key applies to a computer or a service.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e2ad-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e2ad-105">Syntax</span></span>


```C++
typedef enum _KEYSVC_TYPE { 
  KeySvcMachine,
  KeySvcService
} KEYSVC_TYPE;
```



## <a name="constants"></a><span data-ttu-id="0e2ad-106">常數</span><span class="sxs-lookup"><span data-stu-id="0e2ad-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0e2ad-107"><span id="KeySvcMachine"></span><span id="keysvcmachine"></span><span id="KEYSVCMACHINE"></span>**KeySvcMachine**</span><span class="sxs-lookup"><span data-stu-id="0e2ad-107"><span id="KeySvcMachine"></span><span id="keysvcmachine"></span><span id="KEYSVCMACHINE"></span>**KeySvcMachine**</span></span>
</dt> <dd>

<span data-ttu-id="0e2ad-108">機碼適用于電腦。</span><span class="sxs-lookup"><span data-stu-id="0e2ad-108">The key is for a computer.</span></span>

</dd> <dt>

<span data-ttu-id="0e2ad-109"><span id="KeySvcService"></span><span id="keysvcservice"></span><span id="KEYSVCSERVICE"></span>**KeySvcService**</span><span class="sxs-lookup"><span data-stu-id="0e2ad-109"><span id="KeySvcService"></span><span id="keysvcservice"></span><span id="KEYSVCSERVICE"></span>**KeySvcService**</span></span>
</dt> <dd>

<span data-ttu-id="0e2ad-110">服務的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="0e2ad-110">The key is for a service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0e2ad-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e2ad-111">Requirements</span></span>



| <span data-ttu-id="0e2ad-112">需求</span><span class="sxs-lookup"><span data-stu-id="0e2ad-112">Requirement</span></span> | <span data-ttu-id="0e2ad-113">值</span><span class="sxs-lookup"><span data-stu-id="0e2ad-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0e2ad-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0e2ad-114">Minimum supported client</span></span><br/> | <span data-ttu-id="0e2ad-115">都不支援</span><span class="sxs-lookup"><span data-stu-id="0e2ad-115">None supported</span></span><br/>                                                             |
| <span data-ttu-id="0e2ad-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0e2ad-116">Minimum supported server</span></span><br/> | <span data-ttu-id="0e2ad-117">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e2ad-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0e2ad-118">標頭</span><span class="sxs-lookup"><span data-stu-id="0e2ad-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e2ad-119"><dt>Rkeysvcc。h</dt></span><span class="sxs-lookup"><span data-stu-id="0e2ad-119"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e2ad-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0e2ad-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e2ad-121">**RKeyOpenKeyService**</span><span class="sxs-lookup"><span data-stu-id="0e2ad-121">**RKeyOpenKeyService**</span></span>](rkeyopenkeyservice.md)
</dt> </dl>

 

 




