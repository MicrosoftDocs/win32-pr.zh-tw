---
description: 列舉或尋找符合指定準則之外部存放區中的第一個或下一個 CTL。
ms.assetid: 0b465e6e-fb5c-4621-a968-c2cdcab0ea15
title: CertStoreProvFindCTL 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 9454f918c9cbc5b6f90642d46fbb33573b70457f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980579"
---
# <a name="certstoreprovfindctl-callback-function"></a><span data-ttu-id="53ba4-103">CertStoreProvFindCTL 回呼函式</span><span class="sxs-lookup"><span data-stu-id="53ba4-103">CertStoreProvFindCTL callback function</span></span>

<span data-ttu-id="53ba4-104">**CertStoreProvFindCTL** 回呼函式會在 [*外部存放區*](../secgloss/e-gly.md)中列舉或尋找符合指定準則的第一個或下一個 [*CTL*](../secgloss/c-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="53ba4-104">The **CertStoreProvFindCTL** callback function enumerates or finds the first or next [*CTL*](../secgloss/c-gly.md) in an [*external store*](../secgloss/e-gly.md) that matches specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="53ba4-105">語法</span><span class="sxs-lookup"><span data-stu-id="53ba4-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvFindCTL(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCTL_CONTEXT               pPrevCtlContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCTL_CONTEXT               *ppProvCtlContext
);
```



## <a name="parameters"></a><span data-ttu-id="53ba4-106">參數</span><span class="sxs-lookup"><span data-stu-id="53ba4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53ba4-107">*hStoreProv* \[在\]</span><span class="sxs-lookup"><span data-stu-id="53ba4-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53ba4-108">**HCERTSTOREPROV** [*憑證存放區*](../secgloss/c-gly.md)的控制碼。</span><span class="sxs-lookup"><span data-stu-id="53ba4-108">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="53ba4-109">*pFindInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="53ba4-109">*pFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53ba4-110">[**證書 \_ 存儲 \_ >prov \_ 尋找 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)結構的指標，其中包含傳遞至 [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)的所有參數。</span><span class="sxs-lookup"><span data-stu-id="53ba4-110">A pointer to a [**CERT\_STORE\_PROV\_FIND\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) structure containing all the parameters passed to the [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).</span></span> <span data-ttu-id="53ba4-111">。</span><span class="sxs-lookup"><span data-stu-id="53ba4-111">function.</span></span>

</dd> <dt>

<span data-ttu-id="53ba4-112">*pPrevCtlCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="53ba4-112">*pPrevCtlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53ba4-113">找到最後一個 CTL 的 [**ctl \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="53ba4-113">A pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) structure of the last CTL found.</span></span> <span data-ttu-id="53ba4-114">第一次呼叫函式時，此參數應該設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="53ba4-114">On first call to the function, this parameter should be set to **NULL**.</span></span> <span data-ttu-id="53ba4-115">在後續的呼叫中，它應該設定為最後一次呼叫時，在 *ppProvCTLCoNtext* 參數中傳回的指標。</span><span class="sxs-lookup"><span data-stu-id="53ba4-115">On subsequent calls, it should be set to the pointer returned in the *ppProvCTLContext* parameter on the last call.</span></span> <span data-ttu-id="53ba4-116">在這個參數中傳遞的非 **Null** 指標是由回呼函數釋放。</span><span class="sxs-lookup"><span data-stu-id="53ba4-116">A non-**NULL** pointer passed in this parameter is freed by the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="53ba4-117">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="53ba4-117">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53ba4-118">任何需要的旗標值。</span><span class="sxs-lookup"><span data-stu-id="53ba4-118">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="53ba4-119">*ppvStoreProvFindInfo* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="53ba4-119">*ppvStoreProvFindInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="53ba4-120">指向緩衝區指標的指標，以傳回存放區提供者資訊。</span><span class="sxs-lookup"><span data-stu-id="53ba4-120">A pointer to a pointer to buffer to return the store provider information.</span></span> <span data-ttu-id="53ba4-121">（選擇性）回呼可以傳回這個參數中內部尋找資訊的指標。</span><span class="sxs-lookup"><span data-stu-id="53ba4-121">Optionally, the callback can return a pointer to internal find information in this parameter.</span></span> <span data-ttu-id="53ba4-122">在第一次呼叫之後，這個參數會設定為先前呼叫函數所傳回的指標。</span><span class="sxs-lookup"><span data-stu-id="53ba4-122">After the first call, this parameter is set to the pointer returned by the previous call to the function.</span></span>

</dd> <dt>

<span data-ttu-id="53ba4-123">*ppProvCtlCoNtext* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="53ba4-123">*ppProvCtlContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53ba4-124">在成功尋找時，會在此參數中傳回所找到之 CTL 的指標。</span><span class="sxs-lookup"><span data-stu-id="53ba4-124">On a successful find, a pointer to the CTL found is returned in this parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53ba4-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="53ba4-125">Return value</span></span>

<span data-ttu-id="53ba4-126">如果函式成功，則傳回 **TRUE** ，否則會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="53ba4-126">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="53ba4-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="53ba4-127">Requirements</span></span>



| <span data-ttu-id="53ba4-128">需求</span><span class="sxs-lookup"><span data-stu-id="53ba4-128">Requirement</span></span> | <span data-ttu-id="53ba4-129">值</span><span class="sxs-lookup"><span data-stu-id="53ba4-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="53ba4-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="53ba4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="53ba4-131">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53ba4-131">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="53ba4-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="53ba4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="53ba4-133">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53ba4-133">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="53ba4-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53ba4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53ba4-135">**證書 \_ 存儲 \_ >PROV \_ 尋找 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="53ba4-135">**CERT\_STORE\_PROV\_FIND\_INFO**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[<span data-ttu-id="53ba4-136">**CertFindCTLInStore**</span><span class="sxs-lookup"><span data-stu-id="53ba4-136">**CertFindCTLInStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)
</dt> <dt>

[<span data-ttu-id="53ba4-137">**CTL \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="53ba4-137">**CTL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
