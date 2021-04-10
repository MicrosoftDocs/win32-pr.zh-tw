---
title: Win32_RDSHServer 類別的 TestAndSetState 方法
description: 比較目前的狀態與指定的比較元;如果兩者相符，則狀態會設定為新的值。 不論相符的結果為何，也會傳回目前的狀態。
ms.assetid: f1bb0076-251b-4c0d-92f9-1c460e1b26bb
ms.tgt_platform: multiple
keywords:
- TestAndSetState 方法遠端桌面服務
- TestAndSetState 方法遠端桌面服務，Win32_RDSHServer 類別
- Win32_RDSHServer 類別遠端桌面服務，TestAndSetState 方法
topic_type:
- apiref
api_name:
- Win32_RDSHServer.TestAndSetState
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ff4c9b616c2a288f5f39b240d71b2611e25d45f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103985"
---
# <a name="testandsetstate-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="df74b-107">Win32 RDSHServer 類別的 TestAndSetState 方法 \_</span><span class="sxs-lookup"><span data-stu-id="df74b-107">TestAndSetState method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="df74b-108">比較目前的狀態與指定的比較元;如果兩者相符，則狀態會設定為新的值。</span><span class="sxs-lookup"><span data-stu-id="df74b-108">Compares the current state to the specified comparand; if the two match, the state is set to a new value.</span></span> <span data-ttu-id="df74b-109">不論相符的結果為何，也會傳回目前的狀態。</span><span class="sxs-lookup"><span data-stu-id="df74b-109">Regardless of the match, the current state is also returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="df74b-110">語法</span><span class="sxs-lookup"><span data-stu-id="df74b-110">Syntax</span></span>


```mof
uint32 TestAndSetState(
  [in]  uint32 Comparand,
  [in]  uint32 NewState,
  [out] uint32 InitState
);
```



## <a name="parameters"></a><span data-ttu-id="df74b-111">參數</span><span class="sxs-lookup"><span data-stu-id="df74b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df74b-112">*比較元* \[在\]</span><span class="sxs-lookup"><span data-stu-id="df74b-112">*Comparand* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df74b-113">要與目前狀態比較的值;如果這兩個值相符，則狀態會設定為 *NewState*。</span><span class="sxs-lookup"><span data-stu-id="df74b-113">A value to compare to the current state; if the two values match, the state is set to *NewState*.</span></span>

</dd> <dt>

<span data-ttu-id="df74b-114">*NewState* \[在\]</span><span class="sxs-lookup"><span data-stu-id="df74b-114">*NewState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df74b-115">狀態的新值。</span><span class="sxs-lookup"><span data-stu-id="df74b-115">The new value of the state.</span></span>

</dd> <dt>

<span data-ttu-id="df74b-116">*InitState* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="df74b-116">*InitState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df74b-117">在成功或失敗時，會傳回目前的狀態。</span><span class="sxs-lookup"><span data-stu-id="df74b-117">On success or failure, returns the current state.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="df74b-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="df74b-118">Requirements</span></span>



| <span data-ttu-id="df74b-119">需求</span><span class="sxs-lookup"><span data-stu-id="df74b-119">Requirement</span></span> | <span data-ttu-id="df74b-120">值</span><span class="sxs-lookup"><span data-stu-id="df74b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="df74b-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="df74b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="df74b-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="df74b-122">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="df74b-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="df74b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="df74b-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="df74b-124">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="df74b-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="df74b-125">Namespace</span></span><br/>                | <span data-ttu-id="df74b-126">根 \\ cimv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="df74b-126">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="df74b-127">MOF</span><span class="sxs-lookup"><span data-stu-id="df74b-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df74b-128"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="df74b-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="df74b-129">DLL</span><span class="sxs-lookup"><span data-stu-id="df74b-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df74b-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df74b-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="df74b-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df74b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df74b-132">**Win32 \_ RDSHServer**</span><span class="sxs-lookup"><span data-stu-id="df74b-132">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 





