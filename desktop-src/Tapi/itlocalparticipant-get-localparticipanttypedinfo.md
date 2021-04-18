---
description: Get \_ LocalParticipantTypedInfo 方法會取得參與者資訊，例如電子郵件名稱或地理位置。
ms.assetid: 46bb70a7-7dc9-463d-8416-737122412750
title: 'ITLocalParticipant：： get_LocalParticipantTypedInfo 方法 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caabaf503963c09898c06659884fd3ac3858e704
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976162"
---
# <a name="itlocalparticipantget_localparticipanttypedinfo-method"></a><span data-ttu-id="524e9-103">ITLocalParticipant：： get \_ LocalParticipantTypedInfo 方法</span><span class="sxs-lookup"><span data-stu-id="524e9-103">ITLocalParticipant::get\_LocalParticipantTypedInfo method</span></span>

<span data-ttu-id="524e9-104">**Get \_ LocalParticipantTypedInfo** 方法會取得參與者資訊，例如電子郵件名稱或地理位置。</span><span class="sxs-lookup"><span data-stu-id="524e9-104">The **get\_LocalParticipantTypedInfo** method gets participant information, such as e-mail name or geographical location.</span></span>

## <a name="syntax"></a><span data-ttu-id="524e9-105">語法</span><span class="sxs-lookup"><span data-stu-id="524e9-105">Syntax</span></span>


```C++
HRESULT get_LocalParticipantTypedInfo(
  [in]  PARTICIPANT_TYPED_INFO InfoType,
  [out] BSTR                   *ppInfo
);
```



## <a name="parameters"></a><span data-ttu-id="524e9-106">參數</span><span class="sxs-lookup"><span data-stu-id="524e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="524e9-107">*InfoType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="524e9-107">*InfoType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="524e9-108">[**參與者 \_所 \_**](participant-typed-info.md) 需資訊類型的類型資訊識別碼。</span><span class="sxs-lookup"><span data-stu-id="524e9-108">[**PARTICIPANT\_TYPED\_INFO**](participant-typed-info.md) identifier of type of information required.</span></span>

</dd> <dt>

<span data-ttu-id="524e9-109">*ppInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="524e9-109">*ppInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="524e9-110">在成功傳回方法之後，將包含所需資訊的 **BSTR** 指標。</span><span class="sxs-lookup"><span data-stu-id="524e9-110">Pointer to a **BSTR** that will contain the required information following a successful return of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="524e9-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="524e9-111">Return value</span></span>

<span data-ttu-id="524e9-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="524e9-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="524e9-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="524e9-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="524e9-114">備註</span><span class="sxs-lookup"><span data-stu-id="524e9-114">Remarks</span></span>

<span data-ttu-id="524e9-115">應用程式必須使用 [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放配置給 *ppInfo* 參數的記憶體。</span><span class="sxs-lookup"><span data-stu-id="524e9-115">The application must use [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppInfo* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="524e9-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="524e9-116">Requirements</span></span>



| <span data-ttu-id="524e9-117">需求</span><span class="sxs-lookup"><span data-stu-id="524e9-117">Requirement</span></span> | <span data-ttu-id="524e9-118">值</span><span class="sxs-lookup"><span data-stu-id="524e9-118">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="524e9-119">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="524e9-119">TAPI version</span></span><br/> | <span data-ttu-id="524e9-120">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="524e9-120">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="524e9-121">標頭</span><span class="sxs-lookup"><span data-stu-id="524e9-121">Header</span></span><br/>       | <dl> <span data-ttu-id="524e9-122"><dt>Confpriv。h</dt></span><span class="sxs-lookup"><span data-stu-id="524e9-122"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="524e9-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="524e9-123">Library</span></span><br/>      | <dl> <span data-ttu-id="524e9-124"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="524e9-124"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="524e9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="524e9-125">DLL</span></span><br/>          | <dl> <span data-ttu-id="524e9-126"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="524e9-126"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="524e9-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="524e9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="524e9-128">**ITLocalParticipant**</span><span class="sxs-lookup"><span data-stu-id="524e9-128">**ITLocalParticipant**</span></span>](itlocalparticipant.md)
</dt> <dt>

[<span data-ttu-id="524e9-129">**參與者 \_ 輸入 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="524e9-129">**PARTICIPANT\_TYPED\_INFO**</span></span>](participant-typed-info.md)
</dt> </dl>

 

