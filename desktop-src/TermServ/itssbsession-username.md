---
title: ITsSbSession Username 屬性
description: 抓取此會話的使用者名稱。
ms.assetid: 0034e8cc-b67b-4e30-a059-47a269bab0fd
ms.tgt_platform: multiple
keywords:
- Username 屬性遠端桌面服務
- Username 屬性遠端桌面服務，ITsSbSession 介面
- ITsSbSession 介面遠端桌面服務，使用者名稱屬性
topic_type:
- apiref
api_name:
- ITsSbSession.Username
- ITsSbSession.get_Username
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5fb66f0639d659fcb6800680ffc3b3486ad12b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966349"
---
# <a name="itssbsessionusername-property"></a><span data-ttu-id="cee6c-106">ITsSbSession：： Username 屬性</span><span class="sxs-lookup"><span data-stu-id="cee6c-106">ITsSbSession::Username property</span></span>

<span data-ttu-id="cee6c-107">抓取此會話的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="cee6c-107">Retrieves the user name for this session.</span></span>

<span data-ttu-id="cee6c-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="cee6c-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cee6c-109">語法</span><span class="sxs-lookup"><span data-stu-id="cee6c-109">Syntax</span></span>


```C++
HRESULT get_Username(
  [out, retval] BSTR *userName
);
```



## <a name="property-value"></a><span data-ttu-id="cee6c-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="cee6c-110">Property value</span></span>

<span data-ttu-id="cee6c-111">接收此會話之使用者名稱之 **BSTR** 變數的指標。</span><span class="sxs-lookup"><span data-stu-id="cee6c-111">A pointer to a **BSTR** variable that receives the user name for this session.</span></span>

## <a name="requirements"></a><span data-ttu-id="cee6c-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="cee6c-112">Requirements</span></span>



| <span data-ttu-id="cee6c-113">需求</span><span class="sxs-lookup"><span data-stu-id="cee6c-113">Requirement</span></span> | <span data-ttu-id="cee6c-114">值</span><span class="sxs-lookup"><span data-stu-id="cee6c-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cee6c-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cee6c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="cee6c-116">都不支援</span><span class="sxs-lookup"><span data-stu-id="cee6c-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="cee6c-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cee6c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="cee6c-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cee6c-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="cee6c-119">Idl</span><span class="sxs-lookup"><span data-stu-id="cee6c-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cee6c-120"><dt>Sbtsv .idl</dt></span><span class="sxs-lookup"><span data-stu-id="cee6c-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cee6c-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cee6c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cee6c-122">**ITsSbSession**</span><span class="sxs-lookup"><span data-stu-id="cee6c-122">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





