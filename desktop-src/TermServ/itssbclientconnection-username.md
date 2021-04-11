---
title: ITsSbClientConnection UserName 屬性
description: 抓取值，指出起始連接的使用者名稱。
ms.assetid: 74f4b8fb-efd4-46d7-9d2f-dd9ef583eb54
ms.tgt_platform: multiple
keywords:
- UserName 屬性遠端桌面服務
- UserName 屬性遠端桌面服務，ITsSbClientConnection 介面
- ITsSbClientConnection 介面遠端桌面服務，使用者名稱屬性
topic_type:
- apiref
api_name:
- ITsSbClientConnection.UserName
- ITsSbClientConnection.get_UserName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94bd3c1e5bb588ffb276b336cd945f32a0c19afd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317435"
---
# <a name="itssbclientconnectionusername-property"></a><span data-ttu-id="54332-106">ITsSbClientConnection：： UserName 屬性</span><span class="sxs-lookup"><span data-stu-id="54332-106">ITsSbClientConnection::UserName property</span></span>

<span data-ttu-id="54332-107">抓取值，指出起始連接的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="54332-107">Retrieves a value that indicates the name of the user who initiated the connection.</span></span>

<span data-ttu-id="54332-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="54332-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="54332-109">語法</span><span class="sxs-lookup"><span data-stu-id="54332-109">Syntax</span></span>


```C++
HRESULT get_UserName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="54332-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="54332-110">Property value</span></span>

<span data-ttu-id="54332-111">使用者名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="54332-111">A pointer to a user name.</span></span> <span data-ttu-id="54332-112">當您完成使用此字串時，請呼叫 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 函式來釋放它。</span><span class="sxs-lookup"><span data-stu-id="54332-112">When you have finished using the string, free it by calling the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="54332-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="54332-113">Requirements</span></span>



| <span data-ttu-id="54332-114">需求</span><span class="sxs-lookup"><span data-stu-id="54332-114">Requirement</span></span> | <span data-ttu-id="54332-115">值</span><span class="sxs-lookup"><span data-stu-id="54332-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="54332-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="54332-116">Minimum supported client</span></span><br/> | <span data-ttu-id="54332-117">都不支援</span><span class="sxs-lookup"><span data-stu-id="54332-117">None supported</span></span><br/>                                                            |
| <span data-ttu-id="54332-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="54332-118">Minimum supported server</span></span><br/> | <span data-ttu-id="54332-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="54332-119">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="54332-120">Idl</span><span class="sxs-lookup"><span data-stu-id="54332-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="54332-121"><dt>Sbtsv .idl</dt></span><span class="sxs-lookup"><span data-stu-id="54332-121"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54332-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="54332-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54332-123">**ITsSbClientConnection**</span><span class="sxs-lookup"><span data-stu-id="54332-123">**ITsSbClientConnection**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

