---
title: ITsSbClientConnection 網域屬性
description: 抓取值，指出遠端桌面連線 (RDC) 用戶端的功能變數名稱。
ms.assetid: 628f450d-10f4-4405-8d7c-ae58c72c2755
ms.tgt_platform: multiple
keywords:
- 網域屬性遠端桌面服務
- 網域屬性遠端桌面服務、ITsSbClientConnection 介面
- ITsSbClientConnection 介面遠端桌面服務，網域屬性
topic_type:
- apiref
api_name:
- ITsSbClientConnection.Domain
- ITsSbClientConnection.get_Domain
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 678d6fc6838b615faeec9fa36b736b3105b64453
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965941"
---
# <a name="itssbclientconnectiondomain-property"></a><span data-ttu-id="5d779-106">ITsSbClientConnection：:D omain 屬性</span><span class="sxs-lookup"><span data-stu-id="5d779-106">ITsSbClientConnection::Domain property</span></span>

<span data-ttu-id="5d779-107">抓取值，指出遠端桌面連線 (RDC) 用戶端的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="5d779-107">Retrieves a value that indicates the domain name of the Remote Desktop Connection (RDC) client.</span></span>

<span data-ttu-id="5d779-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="5d779-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d779-109">語法</span><span class="sxs-lookup"><span data-stu-id="5d779-109">Syntax</span></span>


```C++
HRESULT get_Domain(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="5d779-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="5d779-110">Property value</span></span>

<span data-ttu-id="5d779-111">包含 RDC 用戶端功能變數名稱之 **BSTR** 變數的指標。</span><span class="sxs-lookup"><span data-stu-id="5d779-111">A pointer to a **BSTR** variable that contains the domain name of the RDC client.</span></span> <span data-ttu-id="5d779-112">當您完成使用此字串時，請呼叫 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 函式來釋放它。</span><span class="sxs-lookup"><span data-stu-id="5d779-112">When you have finished using the string, free it by calling the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d779-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d779-113">Requirements</span></span>



| <span data-ttu-id="5d779-114">需求</span><span class="sxs-lookup"><span data-stu-id="5d779-114">Requirement</span></span> | <span data-ttu-id="5d779-115">值</span><span class="sxs-lookup"><span data-stu-id="5d779-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5d779-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5d779-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5d779-117">都不支援</span><span class="sxs-lookup"><span data-stu-id="5d779-117">None supported</span></span><br/>                                                            |
| <span data-ttu-id="5d779-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5d779-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5d779-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5d779-119">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="5d779-120">Idl</span><span class="sxs-lookup"><span data-stu-id="5d779-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5d779-121"><dt>Sbtsv .idl</dt></span><span class="sxs-lookup"><span data-stu-id="5d779-121"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d779-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d779-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d779-123">**ITsSbClientConnection**</span><span class="sxs-lookup"><span data-stu-id="5d779-123">**ITsSbClientConnection**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

