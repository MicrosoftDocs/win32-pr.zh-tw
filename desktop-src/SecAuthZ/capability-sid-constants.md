---
description: 使用 AllocateAndInitializeSid 函式來定義應用程式的知名功能。
ms.assetid: CD27774F-0B70-4D97-96C9-B247536CC88E
title: '功能 SID 常數 (Winnt. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55809cbb341bcbe60578043778bc824e09b8a295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195573"
---
# <a name="capability-sid-constants"></a>功能 SID 常數

功能 SID 常數會使用 [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) 函式來定義應用程式的知名功能。

<dl> <dt>

<span id="SECURITY_CAPABILITY_INTERNET_CLIENT"></span><span id="security_capability_internet_client"></span>**安全性 \_ 功能 \_ 網際網路 \_ 用戶端**
</dt> <dd> <dl> <dt>

 (0x00000001L) 
</dt> <dt>



帳戶可以從用戶端電腦存取網際網路。


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_INTERNET_CLIENT_SERVER"></span><span id="security_capability_internet_client_server"></span>**安全性 \_ 功能 \_ 網際網路 \_ 用戶端 \_ 伺服器**
</dt> <dd> <dl> <dt>

 (0x00000002L) 
</dt> <dt>



帳戶可以從用戶端和伺服器電腦存取網際網路。


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_PRIVATE_NETWORK_CLIENT_SERVER"></span><span id="security_capability_private_network_client_server"></span>**安全性 \_ 功能 \_ 專用 \_ 網 \_ 用戶端 \_ 伺服器**
</dt> <dd> <dl> <dt>

 (0x00000003L) 
</dt> <dt>



帳戶可以從私人網路存取網際網路。


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_PICTURES_LIBRARY"></span><span id="security_capability_pictures_library"></span>**安全性 \_ 功能 \_ 圖片 \_ 庫**
</dt> <dd> <dl> <dt>

 (0x00000004L) 
</dt> <dt>



帳戶具有圖片媒體櫃的存取權。


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_VIDEOS_LIBRARY"></span><span id="security_capability_videos_library"></span>**安全性 \_ 功能 \_ 影片 \_ 庫**
</dt> <dd> <dl> <dt>

 (0x00000005L) 
</dt> <dt>



帳戶可以存取影片庫。


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_MUSIC_LIBRARY"></span><span id="security_capability_music_library"></span>**安全性 \_ 功能 \_ 音樂 \_ 媒體櫃**
</dt> <dd> <dl> <dt>

 (0x00000006L) 
</dt> <dt>



帳戶具有音樂媒體櫃的存取權。


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_DOCUMENTS_LIBRARY"></span><span id="security_capability_documents_library"></span>**安全性 \_ 功能 \_ 文檔 \_ 庫**
</dt> <dd> <dl> <dt>

 (0x00000007L) 
</dt> <dt>



帳戶可以存取文件庫。


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_ENTERPRISE_AUTHENTICATION"></span><span id="security_capability_enterprise_authentication"></span>**安全性 \_ 功能 \_ 企業 \_ 驗證**
</dt> <dd> <dl> <dt>

 (0x00000008L) 
</dt> <dt>



帳戶可以存取預設的 Windows 認證。


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_SHARED_USER_CERTIFICATES"></span><span id="security_capability_shared_user_certificates"></span>**安全性 \_ 功能 \_ 共用 \_ 使用者 \_ 憑證**
</dt> <dd> <dl> <dt>

 (0x00000009L) 
</dt> <dt>



帳戶可以存取共用使用者憑證。


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_REMOVABLE_STORAGE"></span><span id="security_capability_removable_storage"></span>**安全性 \_ 功能 \_ 可移動 \_ 存儲**
</dt> <dd> <dl> <dt>

 (0x0000000AL) 
</dt> <dt>



帳戶具有卸除式存放裝置的存取權。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

在建立功能 SID 時，您需要在 AllocateAndInitializeSid 函式的呼叫中包含封裝授權單位、安全性 \_ 應用程式 \_ 封裝 \_ 授權 {0,0,0,0,0,15} 單位。 [](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) 此外，您還需要內建功能、安全性 \_ 功能 \_ 基礎 \_ rid (0X00000003L) 和安全性內 \_ 建 \_ 功能 \_ rid \_ 計數 (2L) 的基礎 RID 和 rid 計數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Winnt。h</dt> </dl> |



 

