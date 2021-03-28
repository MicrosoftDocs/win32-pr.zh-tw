---
description: 在與網路位址控制項相關聯的氣球提示中顯示錯誤訊息。
title: 'NCM_DISPLAYERRORTIP 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5ECAB6C3-69FC-4f2a-A9E6-80BC37ED3119
api_name:
- NCM_DISPLAYERRORTIP
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8a3968b9001d74721938190369e6b52cf2368835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991111"
---
# <a name="ncm_displayerrortip-message"></a><span data-ttu-id="b94ba-103">NCM \_ DISPLAYERRORTIP 訊息</span><span class="sxs-lookup"><span data-stu-id="b94ba-103">NCM\_DISPLAYERRORTIP message</span></span>

<span data-ttu-id="b94ba-104">在與網路位址控制項相關聯的氣球提示中顯示錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="b94ba-104">Displays an error message in the balloon tip associated with the network address control.</span></span>


```C++
NCM_DISPLAYERRORTIP

    wParam = 0;

    lParam = 0;            

            
```



## <a name="parameters"></a><span data-ttu-id="b94ba-105">參數</span><span class="sxs-lookup"><span data-stu-id="b94ba-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b94ba-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b94ba-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b94ba-107">必須為零。</span><span class="sxs-lookup"><span data-stu-id="b94ba-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b94ba-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b94ba-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b94ba-109">必須為零。</span><span class="sxs-lookup"><span data-stu-id="b94ba-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b94ba-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="b94ba-110">Return value</span></span>

<span data-ttu-id="b94ba-111">如果此訊息成功，則會 **傳回 \_ [確定]**。</span><span class="sxs-lookup"><span data-stu-id="b94ba-111">If this message succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b94ba-112">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b94ba-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b94ba-113">備註</span><span class="sxs-lookup"><span data-stu-id="b94ba-113">Remarks</span></span>

<span data-ttu-id="b94ba-114">當輸入至控制項的位址未針對以 [**NCM \_ SETALLOWTYPE**](ncm-setallowtype.md) 訊息設定的允許網路位址類型進行驗證時，請傳送此訊息以顯示錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="b94ba-114">Send this message to display an error message when an address typed into the control does not validate against the allowed network address types set with the [**NCM\_SETALLOWTYPE**](ncm-setallowtype.md) message.</span></span> <span data-ttu-id="b94ba-115">使用 [**NCM \_ GETADDRESS**](ncm-getaddress.md) 訊息來驗證位址。</span><span class="sxs-lookup"><span data-stu-id="b94ba-115">Use the [**NCM\_GETADDRESS**](ncm-getaddress.md) message to validate the address.</span></span>

## <a name="requirements"></a><span data-ttu-id="b94ba-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="b94ba-116">Requirements</span></span>



| <span data-ttu-id="b94ba-117">需求</span><span class="sxs-lookup"><span data-stu-id="b94ba-117">Requirement</span></span> | <span data-ttu-id="b94ba-118">值</span><span class="sxs-lookup"><span data-stu-id="b94ba-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b94ba-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b94ba-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b94ba-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b94ba-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b94ba-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b94ba-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b94ba-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b94ba-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b94ba-123">標頭</span><span class="sxs-lookup"><span data-stu-id="b94ba-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b94ba-124"><dt>Shellapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="b94ba-124"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b94ba-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b94ba-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b94ba-126">**NetAddr \_ DisplayErrorTip**</span><span class="sxs-lookup"><span data-stu-id="b94ba-126">**NetAddr\_DisplayErrorTip**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_displayerrortip)
</dt> </dl>

 

 




