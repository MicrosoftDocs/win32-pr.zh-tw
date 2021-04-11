---
title: '其他會話常數 (WSManDisp .h) '
description: 指定編碼、加密和服務主體名稱埠。
ms.assetid: a921b7bc-1f40-427c-971f-c0bc9c9f6887
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagUTF8
- WSManFlagNoEncryption
- WSManFlagEnableSPNServerPort
- WSManFlagUTF16
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 236e69d80db2ad30b8cc2934b6b2016d7eecbed6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105630"
---
# <a name="other-session-constants"></a><span data-ttu-id="b4bbe-103">其他會話常數</span><span class="sxs-lookup"><span data-stu-id="b4bbe-103">Other Session Constants</span></span>

<span data-ttu-id="b4bbe-104">下列清單中所列的常數，位於指定編碼、加密和服務主體名稱埠的 **\_ \_ WSManSessionFlags** 列舉中。</span><span class="sxs-lookup"><span data-stu-id="b4bbe-104">Constants, listed in the following list, in the **\_\_WSManSessionFlags** enumeration that specify encoding, encryption, and service principal name port.</span></span>

<dl> <dt>

<span data-ttu-id="b4bbe-105"><span id="WSManFlagUTF8"></span><span id="wsmanflagutf8"></span><span id="WSMANFLAGUTF8"></span>**WSManFlagUTF8**</span><span class="sxs-lookup"><span data-stu-id="b4bbe-105"><span id="WSManFlagUTF8"></span><span id="wsmanflagutf8"></span><span id="WSMANFLAGUTF8"></span>**WSManFlagUTF8**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4bbe-106">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="b4bbe-106">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="b4bbe-107">以 UTF8 而非 UTF16 傳送要求。</span><span class="sxs-lookup"><span data-stu-id="b4bbe-107">Sends the request in UTF8 rather than UTF16.</span></span>

<span data-ttu-id="b4bbe-108">相關聯的腳本方法是 [**WSMan. SessionFlagUTF8**](wsman-sessionflagutf8.md) ，而 c + + 方法是 [**IWSManEx. SessionFlagUTF8**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagutf8)。</span><span class="sxs-lookup"><span data-stu-id="b4bbe-108">The associated scripting method is [**WSMan.SessionFlagUTF8**](wsman-sessionflagutf8.md) and the C++ method is [**IWSManEx.SessionFlagUTF8**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagutf8).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b4bbe-109"><span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**</span><span class="sxs-lookup"><span data-stu-id="b4bbe-109"><span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4bbe-110">1048576 (0x100000) </span><span class="sxs-lookup"><span data-stu-id="b4bbe-110">1048576 (0x100000)</span></span>
</dt> <dt>



<span data-ttu-id="b4bbe-111">請勿加密透過網路傳送的訊息。</span><span class="sxs-lookup"><span data-stu-id="b4bbe-111">Do not encrypt the messages sent over the network.</span></span> <span data-ttu-id="b4bbe-112">只有 [*在設定接聽程式，*](windows-remote-management-glossary.md) 讓 **AllowUnencrypted** 設為 **True** 時，才允許此設定。</span><span class="sxs-lookup"><span data-stu-id="b4bbe-112">This setting is allowed only if the [*listener*](windows-remote-management-glossary.md) is configured so that **AllowUnencrypted** is set to **True**.</span></span>

<span data-ttu-id="b4bbe-113">相關聯的腳本方法是 [**WSMan. SessionFlagNoEncryption**](wsman-sessionflagnoencryption.md) ，而 c + + 方法是 [**IWSManEx. SessionFlagNoEncryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption)。</span><span class="sxs-lookup"><span data-stu-id="b4bbe-113">The associated scripting method is [**WSMan.SessionFlagNoEncryption**](wsman-sessionflagnoencryption.md) and the C++ method is [**IWSManEx.SessionFlagNoEncryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b4bbe-114"><span id="WSManFlagEnableSPNServerPort"></span><span id="wsmanflagenablespnserverport"></span><span id="WSMANFLAGENABLESPNSERVERPORT"></span>**WSManFlagEnableSPNServerPort**</span><span class="sxs-lookup"><span data-stu-id="b4bbe-114"><span id="WSManFlagEnableSPNServerPort"></span><span id="wsmanflagenablespnserverport"></span><span id="WSMANFLAGENABLESPNSERVERPORT"></span>**WSManFlagEnableSPNServerPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4bbe-115">4194304 (0x400000) </span><span class="sxs-lookup"><span data-stu-id="b4bbe-115">4194304 (0x400000)</span></span>
</dt> <dt>



<span data-ttu-id="b4bbe-116">直接連接到遠端 BMC 硬體（也稱為 [*頻*](windows-remote-management-glossary.md) 外連線）時，請指定服務主體名稱 (SPN) 埠。</span><span class="sxs-lookup"><span data-stu-id="b4bbe-116">Specify the Service Principal Name (SPN) port when connecting directly to remote BMC hardware, also known as an [*out-of-band*](windows-remote-management-glossary.md) connection.</span></span> <span data-ttu-id="b4bbe-117">由於 WinRM 伺服器電腦和 BMC 硬體都可以共用相同的 IP 位址，因此此旗標表示必須使用 SPN 埠號碼來判斷連線是否為服務或直接連線至 BMC。</span><span class="sxs-lookup"><span data-stu-id="b4bbe-117">Because both the WinRM server computer and the BMC hardware can share the same IP address, this flag indicates that the SPN port number must be used to determine whether the connection is to the service or directly to the BMC.</span></span> <span data-ttu-id="b4bbe-118">如需詳細資訊，請參閱 [唯一 spn 的名稱格式](/windows/desktop/AD/name-formats-for-unique-spns)。</span><span class="sxs-lookup"><span data-stu-id="b4bbe-118">For more information, see [Name Formats for Unique SPNs](/windows/desktop/AD/name-formats-for-unique-spns).</span></span>

<span data-ttu-id="b4bbe-119">相關聯的腳本方法是 [**WSMan. SessionFlagEnableSPNServerPort**](wsman-sessionflagenablespnserverport.md) ，而 c + + 方法是 [**IWSManEx. SessionFlagEnableSPNServerPort**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagenablespnserverport)。</span><span class="sxs-lookup"><span data-stu-id="b4bbe-119">The associated scripting method is [**WSMan.SessionFlagEnableSPNServerPort**](wsman-sessionflagenablespnserverport.md) and the C++ method is [**IWSManEx.SessionFlagEnableSPNServerPort**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagenablespnserverport).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b4bbe-120"><span id="WSManFlagUTF16"></span><span id="wsmanflagutf16"></span><span id="WSMANFLAGUTF16"></span>**WSManFlagUTF16**</span><span class="sxs-lookup"><span data-stu-id="b4bbe-120"><span id="WSManFlagUTF16"></span><span id="wsmanflagutf16"></span><span id="WSMANFLAGUTF16"></span>**WSManFlagUTF16**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4bbe-121">0x800000</span><span class="sxs-lookup"><span data-stu-id="b4bbe-121">0x800000</span></span>
</dt> <dt>



<span data-ttu-id="b4bbe-122">將要求傳送至 UTF16。</span><span class="sxs-lookup"><span data-stu-id="b4bbe-122">Sends the request in UTF16.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b4bbe-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="b4bbe-123">Requirements</span></span>



| <span data-ttu-id="b4bbe-124">需求</span><span class="sxs-lookup"><span data-stu-id="b4bbe-124">Requirement</span></span> | <span data-ttu-id="b4bbe-125">值</span><span class="sxs-lookup"><span data-stu-id="b4bbe-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4bbe-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b4bbe-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b4bbe-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b4bbe-127">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="b4bbe-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b4bbe-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b4bbe-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4bbe-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b4bbe-130">標頭</span><span class="sxs-lookup"><span data-stu-id="b4bbe-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4bbe-131"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="b4bbe-131"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b4bbe-132">Idl</span><span class="sxs-lookup"><span data-stu-id="b4bbe-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b4bbe-133"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="b4bbe-133"><dt>WSManDisp.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4bbe-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b4bbe-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4bbe-135">會話常數</span><span class="sxs-lookup"><span data-stu-id="b4bbe-135">Session Constants</span></span>](session-constants.md)
</dt> </dl>

 

