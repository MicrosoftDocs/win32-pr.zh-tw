---
description: 抓取指定的網路位址控制項接受的網路位址類型。
title: 'NCM_GETALLOWTYPE 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1B06463F-0CA6-4e8e-BD3B-917562A6A244
api_name:
- NCM_GETALLOWTYPE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5d93cb3cff575c18764e352da54a717d7c557001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026333"
---
# <a name="ncm_getallowtype-message"></a><span data-ttu-id="bda5a-103">NCM \_ GETALLOWTYPE 訊息</span><span class="sxs-lookup"><span data-stu-id="bda5a-103">NCM\_GETALLOWTYPE message</span></span>

<span data-ttu-id="bda5a-104">抓取指定的網路位址控制項接受的網路位址類型。</span><span class="sxs-lookup"><span data-stu-id="bda5a-104">Retrieves the network address types that a specified network address control accepts.</span></span>


```C++
NCM_GETALLOWTYPE

    wParam = 0;

    lParam = 0;            

            
```



## <a name="parameters"></a><span data-ttu-id="bda5a-105">參數</span><span class="sxs-lookup"><span data-stu-id="bda5a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bda5a-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bda5a-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bda5a-107">必須為零。</span><span class="sxs-lookup"><span data-stu-id="bda5a-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bda5a-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bda5a-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bda5a-109">必須為零。</span><span class="sxs-lookup"><span data-stu-id="bda5a-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bda5a-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="bda5a-110">Return value</span></span>

<span data-ttu-id="bda5a-111">傳回允許的網路位址類型作為一或多個 [**NET \_ 字串**](net-string.md) 常數。</span><span class="sxs-lookup"><span data-stu-id="bda5a-111">Returns the allowed network address types as one or more of the [**NET\_STRING**](net-string.md) constants.</span></span>

## <a name="remarks"></a><span data-ttu-id="bda5a-112">備註</span><span class="sxs-lookup"><span data-stu-id="bda5a-112">Remarks</span></span>

<span data-ttu-id="bda5a-113">傳回的遮罩是在 [**NCM \_ GETADDRESS**](ncm-getaddress.md) 訊息中用來驗證網路位址的準則。</span><span class="sxs-lookup"><span data-stu-id="bda5a-113">The returned mask is the criterion used to validate a network address in the [**NCM\_GETADDRESS**](ncm-getaddress.md) message.</span></span>

<span data-ttu-id="bda5a-114">此訊息僅供網路位址控制使用。</span><span class="sxs-lookup"><span data-stu-id="bda5a-114">Use this message for a network address control only.</span></span> <span data-ttu-id="bda5a-115">若要具現化，請使用 Shellapi 中所定義的類別 **msctls \_ netaddress** 。</span><span class="sxs-lookup"><span data-stu-id="bda5a-115">To instantiate, use the class **msctls\_netaddress** defined in Shellapi.h.</span></span> <span data-ttu-id="bda5a-116">請在執行時間呼叫 [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) ，然後再傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="bda5a-116">Call [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) at run time before sending this message.</span></span> <span data-ttu-id="bda5a-117">這會初始化包含網路位址控制項的通用控制項程式庫。</span><span class="sxs-lookup"><span data-stu-id="bda5a-117">This initializes the common controls library that contains the network address control.</span></span>

## <a name="requirements"></a><span data-ttu-id="bda5a-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="bda5a-118">Requirements</span></span>



| <span data-ttu-id="bda5a-119">需求</span><span class="sxs-lookup"><span data-stu-id="bda5a-119">Requirement</span></span> | <span data-ttu-id="bda5a-120">值</span><span class="sxs-lookup"><span data-stu-id="bda5a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bda5a-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bda5a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bda5a-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bda5a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bda5a-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bda5a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bda5a-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bda5a-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bda5a-125">標頭</span><span class="sxs-lookup"><span data-stu-id="bda5a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bda5a-126"><dt>Shellapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="bda5a-126"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bda5a-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bda5a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bda5a-128">**NCM \_ SETALLOWTYPE**</span><span class="sxs-lookup"><span data-stu-id="bda5a-128">**NCM\_SETALLOWTYPE**</span></span>](ncm-setallowtype.md)
</dt> <dt>

[<span data-ttu-id="bda5a-129">**NetAddr \_ GetAllowType**</span><span class="sxs-lookup"><span data-stu-id="bda5a-129">**NetAddr\_GetAllowType**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getallowtype)
</dt> </dl>

 

 




