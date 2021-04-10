---
title: '連接結構 (NapEnforcementClient .h) '
description: 包含 enforcer 所維護之連接清單的相關資訊。
ms.assetid: 79466099-b567-4268-b9bf-d5e57f4d4900
keywords:
- 連接結構 NAP
topic_type:
- apiref
api_name:
- Connections
api_location:
- NapEnforcementClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e79add74830dfa8ca77fa24a5d3233542a7e553
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935141"
---
# <a name="connections-structure"></a><span data-ttu-id="5e80f-104">連接結構</span><span class="sxs-lookup"><span data-stu-id="5e80f-104">Connections structure</span></span>

> [!Note]  
> <span data-ttu-id="5e80f-105">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="5e80f-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5e80f-106">**連接** 結構包含 enforcer 所維護之連接清單的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5e80f-106">The **Connections** structure contains information about the list of connections maintained by an enforcer.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e80f-107">語法</span><span class="sxs-lookup"><span data-stu-id="5e80f-107">Syntax</span></span>


```C++
typedef struct tagConnections {
  UINT16                          count;
  INapEnforcementClientConnection **connections;
} Connections;
```



## <a name="members"></a><span data-ttu-id="5e80f-108">成員</span><span class="sxs-lookup"><span data-stu-id="5e80f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="5e80f-109">**計數**</span><span class="sxs-lookup"><span data-stu-id="5e80f-109">**count**</span></span>
</dt> <dd>

<span data-ttu-id="5e80f-110">目前由 enforcer 所維護的作用中連接數目，範圍 0 (零) 至 [**maxConnectionCountPerEnforcer**](nap-type-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="5e80f-110">The number of active connections currently maintained by an enforcer within the range 0 (zero) to [**maxConnectionCountPerEnforcer**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e80f-111">**連接**</span><span class="sxs-lookup"><span data-stu-id="5e80f-111">**connections**</span></span>
</dt> <dd>

<span data-ttu-id="5e80f-112">代表用戶端連接之 [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) 介面清單的 COM 指標。</span><span class="sxs-lookup"><span data-stu-id="5e80f-112">A COM pointer to a list of [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interfaces that represent client connections.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5e80f-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e80f-113">Requirements</span></span>



| <span data-ttu-id="5e80f-114">需求</span><span class="sxs-lookup"><span data-stu-id="5e80f-114">Requirement</span></span> | <span data-ttu-id="5e80f-115">值</span><span class="sxs-lookup"><span data-stu-id="5e80f-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e80f-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5e80f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5e80f-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e80f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5e80f-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5e80f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5e80f-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e80f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5e80f-120">標頭</span><span class="sxs-lookup"><span data-stu-id="5e80f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e80f-121"><dt>NapEnforcementClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="5e80f-121"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="5e80f-122">Idl</span><span class="sxs-lookup"><span data-stu-id="5e80f-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5e80f-123"><dt>NapEnforcementClient .idl</dt></span><span class="sxs-lookup"><span data-stu-id="5e80f-123"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e80f-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5e80f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e80f-125">NAP 參考</span><span class="sxs-lookup"><span data-stu-id="5e80f-125">NAP Reference</span></span>](nap-reference.md)
</dt> <dt>

[<span data-ttu-id="5e80f-126">NAP 結構</span><span class="sxs-lookup"><span data-stu-id="5e80f-126">NAP Structures</span></span>](nap-structures.md)
</dt> <dt>

[<span data-ttu-id="5e80f-127">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="5e80f-127">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





