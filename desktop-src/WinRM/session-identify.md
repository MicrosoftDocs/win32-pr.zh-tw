---
title: Session)  (WSManDisp 的方法
description: 查詢遠端電腦，以判斷它是否支援 WS-Management 的通訊協定。
ms.assetid: b86ec9b8-8fc4-4c3e-aca7-2f7d039749df
ms.tgt_platform: multiple
keywords:
- 識別方法 Windows 遠端管理
- 識別方法 Windows 遠端管理、會話物件
- 會話物件 Windows 遠端管理，識別方法
topic_type:
- apiref
api_name:
- Session.Identify
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f1caa5b1e44e4ca65082e33bca4d045e487c96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968591"
---
# <a name="sessionidentify-method"></a><span data-ttu-id="aade9-106">Session。識別方法</span><span class="sxs-lookup"><span data-stu-id="aade9-106">Session.Identify method</span></span>

<span data-ttu-id="aade9-107">**會話。識別** 方法會查詢遠端電腦，以判斷它是否支援 WS-Management 的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="aade9-107">The **Session.Identify** method queries a remote computer to determine if it supports the WS-Management protocol.</span></span> <span data-ttu-id="aade9-108">如需詳細資訊，請參閱偵測 [遠端電腦是否支援 WS-Management 的通訊協定](detecting-whether-a-remote-computer-supports-ws-management-protocol.md)。</span><span class="sxs-lookup"><span data-stu-id="aade9-108">For more information, see [Detecting Whether a Remote Computer Supports WS-Management Protocol](detecting-whether-a-remote-computer-supports-ws-management-protocol.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="aade9-109">語法</span><span class="sxs-lookup"><span data-stu-id="aade9-109">Syntax</span></span>


```VB
Session.Identify( _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="aade9-110">參數</span><span class="sxs-lookup"><span data-stu-id="aade9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aade9-111">*旗標* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="aade9-111">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="aade9-112">若要在經過驗證的模式下傳送要求，請使用來自 **WSManSessionFlags** 列舉的驗證常數。</span><span class="sxs-lookup"><span data-stu-id="aade9-112">To send the request in authenticated mode use authentication constant from the **WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="aade9-113">若要以未驗證的模式傳送，請使用 **WSManFlagUseNoAuthentication**。</span><span class="sxs-lookup"><span data-stu-id="aade9-113">To send in unauthenticated mode, use **WSManFlagUseNoAuthentication**.</span></span> <span data-ttu-id="aade9-114">如需詳細資訊，請參閱 [**驗證常數**](authentication-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="aade9-114">For more information, see [**Authentication Constants**](authentication-constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aade9-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="aade9-115">Return value</span></span>

<span data-ttu-id="aade9-116">XML 字串，這個字串會指定 WS-Management 的通訊協定版本、作業系統廠商，以及要求是否已通過驗證的作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="aade9-116">An XML string that specifies the WS-Management protocol version, the operating system vendor and, if the request was sent authenticated, the operating system version.</span></span>

## <a name="remarks"></a><span data-ttu-id="aade9-117">備註</span><span class="sxs-lookup"><span data-stu-id="aade9-117">Remarks</span></span>

<span data-ttu-id="aade9-118">**會話。識別** 是以定義為 wsmanIdentity 的 [WS-Management 通訊協定](ws-management-protocol.md) 作業為基礎。</span><span class="sxs-lookup"><span data-stu-id="aade9-118">**Session.Identify** is based on the [WS-Management Protocol](ws-management-protocol.md) operation defined as wsmanIdentity.</span></span> <span data-ttu-id="aade9-119">這是在 SOAP 封包中指定，如下所示：</span><span class="sxs-lookup"><span data-stu-id="aade9-119">This is specified in the SOAP packet as follows:</span></span>


```XML
xmlns:wsmid="https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity"
```



## <a name="examples"></a><span data-ttu-id="aade9-120">範例</span><span class="sxs-lookup"><span data-stu-id="aade9-120">Examples</span></span>

<span data-ttu-id="aade9-121">下列 VBScript 範例會將未經驗證的識別要求傳送到相同網域中名為 Remote 的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="aade9-121">The following VBScript example sends an unauthenticated Identify request to the remote computer named Remote in the same domain.</span></span>


```VB
set WSMan = CreateObject("Wsman.Automation")
set Session = WSMan.CreateSession("Remote", _
  WSMan.SessionFlagUseNoAuthentication)
WScript.Echo Session.Identify
```



## <a name="requirements"></a><span data-ttu-id="aade9-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="aade9-122">Requirements</span></span>



| <span data-ttu-id="aade9-123">需求</span><span class="sxs-lookup"><span data-stu-id="aade9-123">Requirement</span></span> | <span data-ttu-id="aade9-124">值</span><span class="sxs-lookup"><span data-stu-id="aade9-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="aade9-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aade9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="aade9-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aade9-126">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="aade9-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aade9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="aade9-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aade9-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="aade9-129">標頭</span><span class="sxs-lookup"><span data-stu-id="aade9-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="aade9-130"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="aade9-130"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="aade9-131">Idl</span><span class="sxs-lookup"><span data-stu-id="aade9-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="aade9-132"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="aade9-132"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="aade9-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="aade9-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="aade9-134"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="aade9-134"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="aade9-135">DLL</span><span class="sxs-lookup"><span data-stu-id="aade9-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aade9-136"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aade9-136"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="aade9-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aade9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aade9-138">**工作階段**</span><span class="sxs-lookup"><span data-stu-id="aade9-138">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="aade9-139">**Iwsmansession.invoke：：識別**</span><span class="sxs-lookup"><span data-stu-id="aade9-139">**IWSManSession::Identify**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify)
</dt> <dt>

[<span data-ttu-id="aade9-140">WS-Management 通訊協定</span><span class="sxs-lookup"><span data-stu-id="aade9-140">WS-Management Protocol</span></span>](ws-management-protocol.md)
</dt> </dl>

 

 





