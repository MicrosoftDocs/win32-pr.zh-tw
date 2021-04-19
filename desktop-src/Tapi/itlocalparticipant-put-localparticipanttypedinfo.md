---
description: Put \_ LocalParticipantTypedInfo 方法會設定參與者資訊。
ms.assetid: c4afd1d3-6fe4-4e5b-a9bf-81b7dffa9914
title: 'ITLocalParticipant：:p ut_LocalParticipantTypedInfo 方法 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77809a9a3858b6a098fa3ff6a93878cf38518f92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000460"
---
# <a name="itlocalparticipantput_localparticipanttypedinfo-method"></a><span data-ttu-id="deddb-103">ITLocalParticipant：:p 的 \_ LocalParticipantTypedInfo 方法</span><span class="sxs-lookup"><span data-stu-id="deddb-103">ITLocalParticipant::put\_LocalParticipantTypedInfo method</span></span>

<span data-ttu-id="deddb-104">**Put \_ LocalParticipantTypedInfo** 方法會設定參與者資訊。</span><span class="sxs-lookup"><span data-stu-id="deddb-104">The **put\_LocalParticipantTypedInfo** method sets participant information.</span></span>

## <a name="syntax"></a><span data-ttu-id="deddb-105">語法</span><span class="sxs-lookup"><span data-stu-id="deddb-105">Syntax</span></span>


```C++
HRESULT put_LocalParticipantTypedInfo(
  [in] PARTICIPANT_TYPED_INFO InfoType,
  [in] BSTR                   ppInfo
);
```



## <a name="parameters"></a><span data-ttu-id="deddb-106">參數</span><span class="sxs-lookup"><span data-stu-id="deddb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="deddb-107">*InfoType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="deddb-107">*InfoType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deddb-108">[**參與者 \_所 \_**](participant-typed-info.md) 需資訊類型的類型資訊識別碼。</span><span class="sxs-lookup"><span data-stu-id="deddb-108">[**PARTICIPANT\_TYPED\_INFO**](participant-typed-info.md) identifier of the type of information required.</span></span>

</dd> <dt>

<span data-ttu-id="deddb-109">*ppInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="deddb-109">*ppInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deddb-110">包含資訊的必要新值的 **BSTR** 。</span><span class="sxs-lookup"><span data-stu-id="deddb-110">**BSTR** containing the required new value for the information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="deddb-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="deddb-111">Return value</span></span>

<span data-ttu-id="deddb-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="deddb-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="deddb-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="deddb-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="deddb-114">備註</span><span class="sxs-lookup"><span data-stu-id="deddb-114">Remarks</span></span>

<span data-ttu-id="deddb-115">應用程式必須使用 [SysAllocString](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) 為 *ppInfo* 參數配置記憶體，並在不再需要該變數時，使用 [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="deddb-115">The application must use [SysAllocString](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *ppInfo* parameter and use [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="deddb-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="deddb-116">Requirements</span></span>



| <span data-ttu-id="deddb-117">需求</span><span class="sxs-lookup"><span data-stu-id="deddb-117">Requirement</span></span> | <span data-ttu-id="deddb-118">值</span><span class="sxs-lookup"><span data-stu-id="deddb-118">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="deddb-119">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="deddb-119">TAPI version</span></span><br/> | <span data-ttu-id="deddb-120">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="deddb-120">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="deddb-121">標頭</span><span class="sxs-lookup"><span data-stu-id="deddb-121">Header</span></span><br/>       | <dl> <span data-ttu-id="deddb-122"><dt>Confpriv。h</dt></span><span class="sxs-lookup"><span data-stu-id="deddb-122"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="deddb-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="deddb-123">Library</span></span><br/>      | <dl> <span data-ttu-id="deddb-124"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="deddb-124"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="deddb-125">DLL</span><span class="sxs-lookup"><span data-stu-id="deddb-125">DLL</span></span><br/>          | <dl> <span data-ttu-id="deddb-126"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="deddb-126"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="deddb-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="deddb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deddb-128">**ITLocalParticipant**</span><span class="sxs-lookup"><span data-stu-id="deddb-128">**ITLocalParticipant**</span></span>](itlocalparticipant.md)
</dt> <dt>

[<span data-ttu-id="deddb-129">**參與者 \_ 輸入 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="deddb-129">**PARTICIPANT\_TYPED\_INFO**</span></span>](participant-typed-info.md)
</dt> </dl>

 

