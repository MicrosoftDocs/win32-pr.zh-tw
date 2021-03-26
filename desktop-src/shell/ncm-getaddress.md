---
description: 指出網路位址是否符合指定的類型和格式。
title: 'NCM_GETADDRESS 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 733CD62D-614C-4ac2-986D-CCFCFF4B1B4D
api_name:
- NCM_GETADDRESS
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5d5effa69a23a61a602efaf1172de09a09889e32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972312"
---
# <a name="ncm_getaddress-message"></a><span data-ttu-id="2973b-103">NCM \_ GETADDRESS 訊息</span><span class="sxs-lookup"><span data-stu-id="2973b-103">NCM\_GETADDRESS message</span></span>

<span data-ttu-id="2973b-104">指出網路位址是否符合指定的類型和格式。</span><span class="sxs-lookup"><span data-stu-id="2973b-104">Indicates whether a network address conforms to a specified type and format.</span></span>


```C++
NCM_GETADDRESS

    wParam = (WPARAM) (PNC_ADDRESS) pv;

    lParam = 0;            

            
```



## <a name="parameters"></a><span data-ttu-id="2973b-105">參數</span><span class="sxs-lookup"><span data-stu-id="2973b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2973b-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2973b-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2973b-107">必須為零。</span><span class="sxs-lookup"><span data-stu-id="2973b-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2973b-108">*pv* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="2973b-108">*pv* \[in, out\]</span></span>
</dt> <dd><span data-ttu-id="2973b-109">如果已驗證 *hwnd* 所指定之控制項中的位址格式和類型，則為用來接收剖析格式之網路位址資訊的 <a href="/windows/win32/api/shellapi/ns-shellapi-nc_address">NC_ADDRESS</a>結構指標。</span><span class="sxs-lookup"><span data-stu-id="2973b-109">A pointer to an <a href="/windows/win32/api/shellapi/ns-shellapi-nc_address">NC_ADDRESS</a> structure to receive network address information in parsed form, if the address format and type in the control specified by *hwnd* are validated.</span></span> <span data-ttu-id="2973b-110">呼叫應用程式負責配置此結構的記憶體。</span><span class="sxs-lookup"><span data-stu-id="2973b-110">The calling application is responsible for allocating the memory for this structure.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2973b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2973b-111">Return value</span></span>

<span data-ttu-id="2973b-112">傳回下列其中一個 **HRESULT** 型別的值。</span><span class="sxs-lookup"><span data-stu-id="2973b-112">Returns one of the following values of type **HRESULT**.</span></span>



| <span data-ttu-id="2973b-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="2973b-113">Return code</span></span>                                                                                                | <span data-ttu-id="2973b-114">Description</span><span class="sxs-lookup"><span data-stu-id="2973b-114">Description</span></span>                                                                                          |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2973b-115"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2973b-115"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="2973b-116">呼叫應用程式無法配置 [**NC \_ 位址**](/windows/win32/api/shellapi/ns-shellapi-nc_address) 結構。</span><span class="sxs-lookup"><span data-stu-id="2973b-116">The calling application failed to allocate a [**NC\_ADDRESS**](/windows/win32/api/shellapi/ns-shellapi-nc_address) structure.</span></span><br/> |
| <dl> <span data-ttu-id="2973b-117"><dt>**\_緩衝區不足的錯誤 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2973b-117"><dt>**ERROR\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="2973b-118">輸出緩衝區太小，無法容納已剖析的網路位址。</span><span class="sxs-lookup"><span data-stu-id="2973b-118">The out buffer is too small to hold the parsed network address.</span></span><br/>                           |
| <dl> <span data-ttu-id="2973b-119"><dt>**錯誤 \_ 不正確 \_ 參數**</dt></span><span class="sxs-lookup"><span data-stu-id="2973b-119"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>   | <span data-ttu-id="2973b-120">網路位址字串不是任何指定的類型。</span><span class="sxs-lookup"><span data-stu-id="2973b-120">The network address string is not of any type specified.</span></span><br/>                                  |
| <dl> <span data-ttu-id="2973b-121"><dt>**錯誤 \_ 成功**</dt></span><span class="sxs-lookup"><span data-stu-id="2973b-121"><dt>**ERROR\_SUCCESS**</dt></span></span> </dl>              | <span data-ttu-id="2973b-122">作業成功。</span><span class="sxs-lookup"><span data-stu-id="2973b-122">The operation was successful.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="2973b-123"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="2973b-123"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="2973b-124">網路位址控制中沒有要驗證的位址。</span><span class="sxs-lookup"><span data-stu-id="2973b-124">There is no address in the network address control to validate.</span></span><br/>                           |



 

## <a name="remarks"></a><span data-ttu-id="2973b-125">備註</span><span class="sxs-lookup"><span data-stu-id="2973b-125">Remarks</span></span>

<span data-ttu-id="2973b-126">使用 **NCM \_ GETADDRESS** 訊息，針對預設的網路位址類型遮罩，驗證網路位址控制項中的網路位址。</span><span class="sxs-lookup"><span data-stu-id="2973b-126">Use the **NCM\_GETADDRESS** message to validate a network address in a network address control against a preset network address type mask.</span></span> <span data-ttu-id="2973b-127">若要具現化，請使用 Shellapi 中所定義的類別 **msctls \_ netaddress** 。</span><span class="sxs-lookup"><span data-stu-id="2973b-127">To instantiate, use the class **msctls\_netaddress** defined in Shellapi.h.</span></span> <span data-ttu-id="2973b-128">請在執行時間呼叫 [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) ，然後再傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="2973b-128">Call [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) at run time before sending this message.</span></span> <span data-ttu-id="2973b-129">這會初始化包含網路位址控制項的通用控制項程式庫。</span><span class="sxs-lookup"><span data-stu-id="2973b-129">This initializes the common controls library that contains the network address control.</span></span>

<span data-ttu-id="2973b-130">此訊息會從網路位址控制項取得網路位址字串、剖析字串，並檢查字串是否符合網路位址類型遮罩。</span><span class="sxs-lookup"><span data-stu-id="2973b-130">This message gets the network address string from a network address control, parses the string, and checks whether the string matches a network address type mask.</span></span> <span data-ttu-id="2973b-131">如果字串符合遮罩，訊息會傳回 S OK，並以剖析的 \_ 形式將字串傳回給呼叫的應用程式 (包括埠號碼、前置長度和其他位址資訊) 使用 *pv* 所指向的 [**NC \_ 位址**](/windows/win32/api/shellapi/ns-shellapi-nc_address)結構。</span><span class="sxs-lookup"><span data-stu-id="2973b-131">If the string matches the mask, the message returns S\_OK and returns the string in parsed form to the calling application (including the port number, prefix length, and other address information), using the [**NC\_ADDRESS**](/windows/win32/api/shellapi/ns-shellapi-nc_address) structure pointed to by *pv*.</span></span> <span data-ttu-id="2973b-132">\_如果呼叫的應用程式無法配置 *pv* 所指向的結構，則此訊息會傳回 E INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="2973b-132">This message returns E\_INVALIDARG if the calling application fails to allocate the structure pointed to by *pv*.</span></span>

<span data-ttu-id="2973b-133">網際網路通訊協定的標記法 (IP) 位址版本4和 6 (v4/v6) 適用于服務和網路，以及使用網域名稱系統 (DNS) 格式的命名網際網路位址和服務。</span><span class="sxs-lookup"><span data-stu-id="2973b-133">Representations of Internet Protocol (IP) address versions 4 and 6 (v4/v6) for services and networks, as well as named Internet addresses and services using Domain Name System (DNS) format are parsed.</span></span> <span data-ttu-id="2973b-134">如果網路位址字串代表 (DNS) 或服務的名稱主機名稱，則 [**NC \_ 位址**](/windows/win32/api/shellapi/ns-shellapi-nc_address)之 **PrefixLength** 成員中傳回的值為零。</span><span class="sxs-lookup"><span data-stu-id="2973b-134">If the network address string represents a named host name (DNS) or service, the value returned in the **PrefixLength** member of [**NC\_ADDRESS**](/windows/win32/api/shellapi/ns-shellapi-nc_address) is zero.</span></span>

<span data-ttu-id="2973b-135">請先使用 [**NCM \_ SETALLOWTYPE**](ncm-setallowtype.md) 訊息設定網路位址類型遮罩，然後再傳送 **NCM \_ GETADDRESS** 宏。</span><span class="sxs-lookup"><span data-stu-id="2973b-135">Set the network address type mask using the [**NCM\_SETALLOWTYPE**](ncm-setallowtype.md) message before you send the **NCM\_GETADDRESS** macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="2973b-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="2973b-136">Requirements</span></span>



| <span data-ttu-id="2973b-137">需求</span><span class="sxs-lookup"><span data-stu-id="2973b-137">Requirement</span></span> | <span data-ttu-id="2973b-138">值</span><span class="sxs-lookup"><span data-stu-id="2973b-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2973b-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2973b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="2973b-140">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2973b-140">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2973b-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2973b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="2973b-142">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2973b-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2973b-143">標頭</span><span class="sxs-lookup"><span data-stu-id="2973b-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="2973b-144"><dt>Shellapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="2973b-144"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2973b-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2973b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2973b-146">**NCM \_ GETALLOWTYPE**</span><span class="sxs-lookup"><span data-stu-id="2973b-146">**NCM\_GETALLOWTYPE**</span></span>](ncm-getallowtype.md)
</dt> <dt>

[<span data-ttu-id="2973b-147">**NetAddr \_ GetAddress**</span><span class="sxs-lookup"><span data-stu-id="2973b-147">**NetAddr\_GetAddress**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getaddress)
</dt> </dl>

 

 




