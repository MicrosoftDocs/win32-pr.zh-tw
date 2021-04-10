---
title: '存取旗標 (Accctrl.h .h) '
description: 這些值會指出存取清單中的專案是否描述允許或拒絕的許可權。
ms.assetid: 460d2c72-3315-4b4c-928e-4bb0640acbe5
topic_type:
- apiref
api_name:
- ACTRL_ACCESS_ALLOWED
- ACTRL_ACCESS_DENIED
api_location:
- AccCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5972bf95efc675d6dd9c2e58c0b7d25c8c305371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106320"
---
# <a name="access-flags"></a><span data-ttu-id="32b3a-103">存取旗標</span><span class="sxs-lookup"><span data-stu-id="32b3a-103">Access Flags</span></span>

<span data-ttu-id="32b3a-104">這些值會指出存取清單中的專案是否描述允許或拒絕的許可權。</span><span class="sxs-lookup"><span data-stu-id="32b3a-104">These values indicate whether an entry in the access list describes rights that are allowed or denied.</span></span>



| <span data-ttu-id="32b3a-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="32b3a-105">Constant/value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="32b3a-106">Description</span><span class="sxs-lookup"><span data-stu-id="32b3a-106">Description</span></span>                                   |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------|
| <span id="ACTRL_ACCESS_ALLOWED"></span><span id="actrl_access_allowed"></span><dl> <span data-ttu-id="32b3a-107"><dt>**ACTRL \_存取 \_ 允許**</dt>的 <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="32b3a-107"><dt>**ACTRL\_ACCESS\_ALLOWED**</dt> <dt>0x00000000</dt></span></span> </dl> | <span data-ttu-id="32b3a-108">表示允許存取的專案。</span><span class="sxs-lookup"><span data-stu-id="32b3a-108">Indicates an access-allowed entry.</span></span><br/> |
| <span id="ACTRL_ACCESS_DENIED"></span><span id="actrl_access_denied"></span><dl> <span data-ttu-id="32b3a-109"><dt>**ACTRL \_\_拒絕存取**</dt> <dt>0x10000000</dt></span><span class="sxs-lookup"><span data-stu-id="32b3a-109"><dt>**ACTRL\_ACCESS\_DENIED**</dt> <dt>0x10000000</dt></span></span> </dl>    | <span data-ttu-id="32b3a-110">表示拒絕存取的專案。</span><span class="sxs-lookup"><span data-stu-id="32b3a-110">Indicates an access-denied entry.</span></span><br/>  |



## <a name="requirements"></a><span data-ttu-id="32b3a-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="32b3a-111">Requirements</span></span>



| <span data-ttu-id="32b3a-112">需求</span><span class="sxs-lookup"><span data-stu-id="32b3a-112">Requirement</span></span> | <span data-ttu-id="32b3a-113">值</span><span class="sxs-lookup"><span data-stu-id="32b3a-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="32b3a-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="32b3a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="32b3a-115">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32b3a-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="32b3a-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="32b3a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="32b3a-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32b3a-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="32b3a-118">標頭</span><span class="sxs-lookup"><span data-stu-id="32b3a-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="32b3a-119"><dt>Accctrl.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="32b3a-119"><dt>AccCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32b3a-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32b3a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32b3a-121">**ACTRL \_ 存取 \_ 專案**</span><span class="sxs-lookup"><span data-stu-id="32b3a-121">**ACTRL\_ACCESS\_ENTRY**</span></span>](/windows/desktop/api/AccCtrl/ns-accctrl-actrl_access_entrya)
</dt> </dl>

 

 





