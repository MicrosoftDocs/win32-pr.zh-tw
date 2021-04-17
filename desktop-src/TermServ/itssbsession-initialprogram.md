---
title: ITsSbSession InitialProgram 屬性
description: 捕獲或指定此會話的初始程式。
ms.assetid: c299c4f7-3c5f-468f-9fc7-81eac322dfa2
ms.tgt_platform: multiple
keywords:
- InitialProgram 屬性遠端桌面服務
- InitialProgram 屬性遠端桌面服務，ITsSbSession 介面
- ITsSbSession 介面遠端桌面服務，InitialProgram 屬性
topic_type:
- apiref
api_name:
- ITsSbSession.InitialProgram
- ITsSbSession.get_InitialProgram
- ITsSbSession.put_InitialProgram
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 307f8bb4330caf4b84b8650c9ccc2551c94da76d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465316"
---
# <a name="itssbsessioninitialprogram-property"></a><span data-ttu-id="a54c2-106">ITsSbSession：： InitialProgram 屬性</span><span class="sxs-lookup"><span data-stu-id="a54c2-106">ITsSbSession::InitialProgram property</span></span>

<span data-ttu-id="a54c2-107">捕獲或指定此會話的初始程式。</span><span class="sxs-lookup"><span data-stu-id="a54c2-107">Retrieves or specifies the initial program for this session.</span></span> <span data-ttu-id="a54c2-108">初始程式是在使用者會話啟動時啟動的程式。</span><span class="sxs-lookup"><span data-stu-id="a54c2-108">The initial program is the program that is launched when the user session starts.</span></span>

<span data-ttu-id="a54c2-109">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="a54c2-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a54c2-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="a54c2-110">Syntax</span></span>


```C++
HRESULT put_InitialProgram(
  [in]          BSTR Application
);

HRESULT get_InitialProgram(
  [out, retval] BSTR *app
);
```



## <a name="property-value"></a><span data-ttu-id="a54c2-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="a54c2-111">Property value</span></span>

<span data-ttu-id="a54c2-112">包含初始程式的 **BSTR** 變數。</span><span class="sxs-lookup"><span data-stu-id="a54c2-112">A **BSTR** variable that contains the initial program.</span></span>

## <a name="requirements"></a><span data-ttu-id="a54c2-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="a54c2-113">Requirements</span></span>



| <span data-ttu-id="a54c2-114">需求</span><span class="sxs-lookup"><span data-stu-id="a54c2-114">Requirement</span></span> | <span data-ttu-id="a54c2-115">值</span><span class="sxs-lookup"><span data-stu-id="a54c2-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a54c2-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a54c2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a54c2-117">都不支援</span><span class="sxs-lookup"><span data-stu-id="a54c2-117">None supported</span></span><br/>                                                            |
| <span data-ttu-id="a54c2-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a54c2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a54c2-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a54c2-119">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="a54c2-120">Idl</span><span class="sxs-lookup"><span data-stu-id="a54c2-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a54c2-121"><dt>Sbtsv .idl</dt></span><span class="sxs-lookup"><span data-stu-id="a54c2-121"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a54c2-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a54c2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a54c2-123">**ITsSbSession**</span><span class="sxs-lookup"><span data-stu-id="a54c2-123">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





