---
description: 抓取憑證信任清單 (CTL) 的指定屬性。
ms.assetid: 65309715-65b4-4608-960d-3404e68800a2
title: CertStoreProvGetCTLProperty 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCTLProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: e30a9e735d44fc5681d5cd3932baaf3cc90aa30d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106999921"
---
# <a name="certstoreprovgetctlproperty-callback-function"></a><span data-ttu-id="0cfa1-103">CertStoreProvGetCTLProperty 回呼函式</span><span class="sxs-lookup"><span data-stu-id="0cfa1-103">CertStoreProvGetCTLProperty callback function</span></span>

<span data-ttu-id="0cfa1-104">**CertStoreProvGetCTLProperty** 回呼函式會抓取 [*憑證信任清單*](../secgloss/c-gly.md) (CTL) 的指定屬性。</span><span class="sxs-lookup"><span data-stu-id="0cfa1-104">The **CertStoreProvGetCTLProperty** callback function retrieves a specified property of a [*certificate trust list*](../secgloss/c-gly.md) (CTL).</span></span>

## <a name="syntax"></a><span data-ttu-id="0cfa1-105">語法</span><span class="sxs-lookup"><span data-stu-id="0cfa1-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvGetCTLProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCTL_CONTEXT  pCtlContext,
  _In_    DWORD          dwPropId,
  _In_    DWORD          dwFlags,
  _Out_   void           *pvData,
  _Inout_ DWORD          *pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="0cfa1-106">參數</span><span class="sxs-lookup"><span data-stu-id="0cfa1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cfa1-107">*hStoreProv* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0cfa1-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cfa1-108">[*憑證存放區*](../secgloss/c-gly.md)的 **HCERTSTOREPROV** 控制碼。</span><span class="sxs-lookup"><span data-stu-id="0cfa1-108">A **HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="0cfa1-109">*pCtlCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0cfa1-109">*pCtlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cfa1-110">[**CTL \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="0cfa1-110">A pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0cfa1-111">*dwPropId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0cfa1-111">*dwPropId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cfa1-112">表示屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="0cfa1-112">Indicates a property identifier.</span></span>

</dd> <dt>

<span data-ttu-id="0cfa1-113">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0cfa1-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cfa1-114">任何需要的旗標值。</span><span class="sxs-lookup"><span data-stu-id="0cfa1-114">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="0cfa1-115">*pvData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0cfa1-115">*pvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cfa1-116">緩衝區的指標，其中包含要由函式傳回之 [**CTL \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="0cfa1-116">A pointer to a buffer to contain the pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) structure to be returned by the function.</span></span> <span data-ttu-id="0cfa1-117">若要在為緩衝區配置記憶體之前取得 *pcbData* 的值，在第一次呼叫函式時，此參數可以設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="0cfa1-117">To get the value of *pcbData* before allocating memory for the buffer, this parameter can be set to **NULL** on a first call to the function.</span></span>

</dd> <dt>

<span data-ttu-id="0cfa1-118">*pcbData* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="0cfa1-118">*pcbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cfa1-119">**DWORD** 的指標，表示 *pvData* 緩衝區的長度。</span><span class="sxs-lookup"><span data-stu-id="0cfa1-119">A pointer to a **DWORD** that indicates the length of the *pvData* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cfa1-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="0cfa1-120">Return value</span></span>

<span data-ttu-id="0cfa1-121">如果函式成功，函數會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="0cfa1-121">If the function succeeds, the function returns nonzero.</span></span>

<span data-ttu-id="0cfa1-122">如果函式失敗，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="0cfa1-122">If the function fails, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cfa1-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="0cfa1-123">Requirements</span></span>



| <span data-ttu-id="0cfa1-124">需求</span><span class="sxs-lookup"><span data-stu-id="0cfa1-124">Requirement</span></span> | <span data-ttu-id="0cfa1-125">值</span><span class="sxs-lookup"><span data-stu-id="0cfa1-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0cfa1-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0cfa1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0cfa1-127">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0cfa1-127">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="0cfa1-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0cfa1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0cfa1-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0cfa1-129">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0cfa1-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0cfa1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cfa1-131">**CTL \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="0cfa1-131">**CTL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
