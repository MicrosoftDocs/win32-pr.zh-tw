---
description: 從存放區刪除 CTL 之前，由 CertDeleteCTLFromStore 呼叫。
ms.assetid: 6cda772f-7e94-414d-99fc-a90451ac0ccf
title: CertStoreProvDeleteCTL 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvDeleteCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: abeea0fdc3b6d77974b2c057d0e2ea98fe11e63a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848908"
---
# <a name="certstoreprovdeletectl-callback-function"></a><span data-ttu-id="77ad7-103">CertStoreProvDeleteCTL 回呼函式</span><span class="sxs-lookup"><span data-stu-id="77ad7-103">CertStoreProvDeleteCTL callback function</span></span>

<span data-ttu-id="77ad7-104">從存放區刪除 CTL 之前， [**CertDeleteCTLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore)會呼叫 **CertStoreProvDeleteCTL** 回呼函數。</span><span class="sxs-lookup"><span data-stu-id="77ad7-104">The **CertStoreProvDeleteCTL** callback function is called by [**CertDeleteCTLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore) before deleting a CTL from the store.</span></span> <span data-ttu-id="77ad7-105">此函數會決定是否可刪除 CTL。</span><span class="sxs-lookup"><span data-stu-id="77ad7-105">This function determines whether a CTL can be deleted.</span></span>

## <a name="syntax"></a><span data-ttu-id="77ad7-106">語法</span><span class="sxs-lookup"><span data-stu-id="77ad7-106">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvDeleteCTL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCTL_CONTEXT  pCtlContext,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="77ad7-107">參數</span><span class="sxs-lookup"><span data-stu-id="77ad7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77ad7-108">*hStoreProv* \[在\]</span><span class="sxs-lookup"><span data-stu-id="77ad7-108">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77ad7-109">**HCERTSTOREPROV** [*憑證存放區*](../secgloss/c-gly.md)的控制碼。</span><span class="sxs-lookup"><span data-stu-id="77ad7-109">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="77ad7-110">*pCtlCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="77ad7-110">*pCtlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77ad7-111">[**CTL \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="77ad7-111">A pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="77ad7-112">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="77ad7-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77ad7-113">任何需要的旗標值。</span><span class="sxs-lookup"><span data-stu-id="77ad7-113">Any needed flag values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77ad7-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="77ad7-114">Return value</span></span>

<span data-ttu-id="77ad7-115">如果可以從存放區刪除 CTL， **則傳回 TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="77ad7-115">Returns **TRUE** if a CTL can be deleted from the store.</span></span>

## <a name="requirements"></a><span data-ttu-id="77ad7-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="77ad7-116">Requirements</span></span>



| <span data-ttu-id="77ad7-117">需求</span><span class="sxs-lookup"><span data-stu-id="77ad7-117">Requirement</span></span> | <span data-ttu-id="77ad7-118">值</span><span class="sxs-lookup"><span data-stu-id="77ad7-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="77ad7-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="77ad7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="77ad7-120">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="77ad7-120">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="77ad7-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="77ad7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="77ad7-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="77ad7-122">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 
