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
ms.openlocfilehash: fcd9d2cf44063dfb1a7ec1bfcbb0fe785d1747d34e84ef2c2d8c78598e6e6b0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743323"
---
# <a name="other-session-constants"></a>其他會話常數

下列清單中所列的常數，位於指定編碼、加密和服務主體名稱埠的 **\_ \_ WSManSessionFlags** 列舉中。

<dl> <dt>

<span id="WSManFlagUTF8"></span><span id="wsmanflagutf8"></span><span id="WSMANFLAGUTF8"></span>**WSManFlagUTF8**
</dt> <dd> <dl> <dt>

1 (0x1) 
</dt> <dt>



以 UTF8 而非 UTF16 傳送要求。

相關聯的腳本方法是 [**WSMan. SessionFlagUTF8**](wsman-sessionflagutf8.md) ，而 c + + 方法是 [**IWSManEx. SessionFlagUTF8**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagutf8)。


</dt> </dl> </dd> <dt>

<span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**
</dt> <dd> <dl> <dt>

1048576 (0x100000) 
</dt> <dt>



請勿加密透過網路傳送的訊息。 只有 [*在設定接聽程式，*](windows-remote-management-glossary.md) 讓 **AllowUnencrypted** 設為 **True** 時，才允許此設定。

相關聯的腳本方法是 [**WSMan. SessionFlagNoEncryption**](wsman-sessionflagnoencryption.md) ，而 c + + 方法是 [**IWSManEx. SessionFlagNoEncryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption)。


</dt> </dl> </dd> <dt>

<span id="WSManFlagEnableSPNServerPort"></span><span id="wsmanflagenablespnserverport"></span><span id="WSMANFLAGENABLESPNSERVERPORT"></span>**WSManFlagEnableSPNServerPort**
</dt> <dd> <dl> <dt>

4194304 (0x400000) 
</dt> <dt>



直接連接到遠端 BMC 硬體（也稱為 [*頻*](windows-remote-management-glossary.md) 外連線）時，請指定服務主體名稱 (SPN) 埠。 由於 WinRM 伺服器電腦和 BMC 硬體都可以共用相同的 IP 位址，因此此旗標表示必須使用 SPN 埠號碼來判斷連線是否為服務或直接連線至 BMC。 如需詳細資訊，請參閱 [唯一 spn 的名稱格式](/windows/desktop/AD/name-formats-for-unique-spns)。

相關聯的腳本方法是 [**WSMan. SessionFlagEnableSPNServerPort**](wsman-sessionflagenablespnserverport.md) ，而 c + + 方法是 [**IWSManEx. SessionFlagEnableSPNServerPort**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagenablespnserverport)。


</dt> </dl> </dd> <dt>

<span id="WSManFlagUTF16"></span><span id="wsmanflagutf16"></span><span id="WSMANFLAGUTF16"></span>**WSManFlagUTF16**
</dt> <dd> <dl> <dt>

0x800000
</dt> <dt>



將要求傳送至 UTF16。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>WSManDisp。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[會話常數](session-constants.md)
</dt> </dl>

 

