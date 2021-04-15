---
title: ITsSbSession 狀態屬性
description: 捕獲或指定會話狀態。
ms.assetid: 4e769ff7-2bd5-4fcb-b2d7-4dedc853482b
ms.tgt_platform: multiple
keywords:
- State 屬性遠端桌面服務
- State 屬性遠端桌面服務，ITsSbSession 介面
- ITsSbSession 介面遠端桌面服務，State 屬性
topic_type:
- apiref
api_name:
- ITsSbSession.State
- ITsSbSession.get_State
- ITsSbSession.put_State
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb939a518ab1050d932349cd70c85bcd22edf3d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466897"
---
# <a name="itssbsessionstate-property"></a><span data-ttu-id="20e95-106">ITsSbSession：： State 屬性</span><span class="sxs-lookup"><span data-stu-id="20e95-106">ITsSbSession::State property</span></span>

<span data-ttu-id="20e95-107">捕獲或指定會話狀態。</span><span class="sxs-lookup"><span data-stu-id="20e95-107">Retrieves or specifies the session state.</span></span>

<span data-ttu-id="20e95-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="20e95-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="20e95-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="20e95-109">Syntax</span></span>


```C++
HRESULT put_State(
  [in]          TSSESSION_STATE State
);

HRESULT get_State(
  [out, retval] TSSESSION_STATE *pState
);
```



## <a name="property-value"></a><span data-ttu-id="20e95-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="20e95-110">Property value</span></span>

<span data-ttu-id="20e95-111">[**TSSESSION \_ 狀態**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-tssession_state)列舉的值，表示會話的狀態。</span><span class="sxs-lookup"><span data-stu-id="20e95-111">A value of the [**TSSESSION\_STATE**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-tssession_state) enumeration that indicates the state of a session.</span></span>

## <a name="requirements"></a><span data-ttu-id="20e95-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="20e95-112">Requirements</span></span>



| <span data-ttu-id="20e95-113">需求</span><span class="sxs-lookup"><span data-stu-id="20e95-113">Requirement</span></span> | <span data-ttu-id="20e95-114">值</span><span class="sxs-lookup"><span data-stu-id="20e95-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="20e95-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="20e95-115">Minimum supported client</span></span><br/> | <span data-ttu-id="20e95-116">都不支援</span><span class="sxs-lookup"><span data-stu-id="20e95-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="20e95-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="20e95-117">Minimum supported server</span></span><br/> | <span data-ttu-id="20e95-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="20e95-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="20e95-119">Idl</span><span class="sxs-lookup"><span data-stu-id="20e95-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="20e95-120"><dt>Sbtsv .idl</dt></span><span class="sxs-lookup"><span data-stu-id="20e95-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20e95-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="20e95-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20e95-122">**ITsSbSession**</span><span class="sxs-lookup"><span data-stu-id="20e95-122">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> <dt>

[<span data-ttu-id="20e95-123">**TSSESSION \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="20e95-123">**TSSESSION\_STATE**</span></span>](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-tssession_state)
</dt> </dl>

 

 





