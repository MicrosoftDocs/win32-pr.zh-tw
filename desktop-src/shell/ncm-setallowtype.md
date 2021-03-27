---
description: 設定指定的網路位址控制項接受的網路位址類型。
title: 'NCM_SETALLOWTYPE 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FD998452-047A-4aea-A08E-8F6F8C30115B
api_name:
- NCM_SETALLOWTYPE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d9cc822e07022a01439fbe7e41243bd1b78e636b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691204"
---
# <a name="ncm_setallowtype-message"></a><span data-ttu-id="e8281-103">NCM \_ SETALLOWTYPE 訊息</span><span class="sxs-lookup"><span data-stu-id="e8281-103">NCM\_SETALLOWTYPE message</span></span>

<span data-ttu-id="e8281-104">設定指定的網路位址控制項接受的網路位址類型。</span><span class="sxs-lookup"><span data-stu-id="e8281-104">Sets the network address types that a specified network address control accepts.</span></span>


```C++
NCM_SETALLOWTYPE

    wParam = (WPARAM) (DWORD) addrMask;

    lParam = 0;            

            
```



## <a name="parameters"></a><span data-ttu-id="e8281-105">參數</span><span class="sxs-lookup"><span data-stu-id="e8281-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8281-106">*addrMask* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e8281-106">*addrMask* \[in\]</span></span>
</dt> <dd><span data-ttu-id="e8281-107">將網路位址類型指定為一或多個 <a href="net-string.md">**NET \_ 字串**</a> 常數。</span><span class="sxs-lookup"><span data-stu-id="e8281-107">Specifies the network address types as one or more of the <a href="net-string.md">**NET\_STRING**</a> constants.</span></span></dd> <dt>

<span data-ttu-id="e8281-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e8281-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e8281-109">必須為零。</span><span class="sxs-lookup"><span data-stu-id="e8281-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8281-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="e8281-110">Return value</span></span>

<span data-ttu-id="e8281-111">\_如果成功，則傳回 [確定]，否則傳回錯誤值。</span><span class="sxs-lookup"><span data-stu-id="e8281-111">Returns S\_OK if successful, or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8281-112">備註</span><span class="sxs-lookup"><span data-stu-id="e8281-112">Remarks</span></span>

<span data-ttu-id="e8281-113">遮罩集是在 [**NCM \_ GETADDRESS**](ncm-getaddress.md) 訊息中用來驗證網路位址的準則。</span><span class="sxs-lookup"><span data-stu-id="e8281-113">The mask set is the criterion used to validate a network address in the [**NCM\_GETADDRESS**](ncm-getaddress.md) message.</span></span>

<span data-ttu-id="e8281-114">此訊息僅供網路位址控制使用。</span><span class="sxs-lookup"><span data-stu-id="e8281-114">Use this message for a network address control only.</span></span> <span data-ttu-id="e8281-115">若要具現化，請使用 Shellapi 中所定義的類別 **msctls \_ netaddress** 。</span><span class="sxs-lookup"><span data-stu-id="e8281-115">To instantiate, use the class **msctls\_netaddress** defined in Shellapi.h.</span></span> <span data-ttu-id="e8281-116">請在執行時間呼叫 [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) ，然後再傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="e8281-116">Call [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) at run time before sending this message.</span></span> <span data-ttu-id="e8281-117">這會初始化包含網路位址控制項的通用控制項程式庫。</span><span class="sxs-lookup"><span data-stu-id="e8281-117">This initializes the common controls library that contains the network address control.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8281-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8281-118">Requirements</span></span>



| <span data-ttu-id="e8281-119">需求</span><span class="sxs-lookup"><span data-stu-id="e8281-119">Requirement</span></span> | <span data-ttu-id="e8281-120">值</span><span class="sxs-lookup"><span data-stu-id="e8281-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8281-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e8281-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e8281-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e8281-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e8281-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e8281-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e8281-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e8281-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e8281-125">標頭</span><span class="sxs-lookup"><span data-stu-id="e8281-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8281-126"><dt>Shellapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="e8281-126"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8281-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8281-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8281-128">**NCM \_ GETALLOWTYPE**</span><span class="sxs-lookup"><span data-stu-id="e8281-128">**NCM\_GETALLOWTYPE**</span></span>](ncm-getallowtype.md)
</dt> <dt>

[<span data-ttu-id="e8281-129">**NetAddr \_ SetAllowType**</span><span class="sxs-lookup"><span data-stu-id="e8281-129">**NetAddr\_SetAllowType**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype)
</dt> </dl>

 

 




