---
title: 'RAS_PORT_STATISTICS 結構 (Rassapi .h) '
description: RAS \_ 埠 \_ 統計結構會報告 ras 伺服器為連線埠收集的統計資料。
ms.assetid: c42c7059-ff92-4f49-a86e-2f47a083aa8e
keywords:
- RAS_PORT_STATISTICS 結構 RAS
- PRAS_PORT_STATISTICS 結構指標 RAS
topic_type:
- apiref
api_name:
- RAS_PORT_STATISTICS
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85e60fb001da3f8401e47c366eecc86aced22b77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966318"
---
# <a name="ras_port_statistics-structure"></a>RAS \_ 埠 \_ 統計資料結構

\[Windows Vista 不支援 **RAS \_ 埠 \_ 統計** 結構。\]

**Ras \_ 埠 \_ 統計** 結構會報告 ras 伺服器為連線埠收集的統計資料。 RAS 伺服器會在每次連線埠時重設各種統計資料計數器。 呼叫 [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md) 函數，以強制 RAS 伺服器重設統計資料計數器。

針對屬於多重連結連接的埠，此結構提供兩組統計資料。 第一個集合包含連接中所有埠的累計統計資料。 連接中的所有埠都有相同的統計資料。 第二個集合只包含此埠的統計資料。 如果埠不是多重連結連接的一部分，則這兩組統計資料都有相同的資訊。 若要判斷埠是否為多重連結連線的一部分，請檢查埠 \_ 的 [**RAS \_ 埠 \_ 0**](ras-port-0-str.md)結構 **旗標** 成員中的埠多連結位。

## <a name="syntax"></a>語法


```C++
typedef struct _RAS_PORT_STATISTICS {
  DWORD dwBytesXmited;
  DWORD dwBytesRcved;
  DWORD dwFramesXmited;
  DWORD dwFramesRcved;
  DWORD dwCrcErr;
  DWORD dwTimeoutErr;
  DWORD dwAlignmentErr;
  DWORD dwHardwareOverrunErr;
  DWORD dwFramingErr;
  DWORD dwBufferOverrunErr;
  DWORD dwBytesXmitedUncompressed;
  DWORD dwBytesRcvedUncompressed;
  DWORD dwBytesXmitedCompressed;
  DWORD dwBytesRcvedCompressed;
  DWORD dwPortBytesXmited;
  DWORD dwPortBytesRcved;
  DWORD dwPortFramesXmited;
  DWORD dwPortFramesRcved;
  DWORD dwPortCrcErr;
  DWORD dwPortTimeoutErr;
  DWORD dwPortAlignmentErr;
  DWORD dwPortHardwareOverrunErr;
  DWORD dwPortFramingErr;
  DWORD dwPortBufferOverrunErr;
  DWORD dwPortBytesXmitedUncompressed;
  DWORD dwPortBytesRcvedUncompressed;
  DWORD dwPortBytesXmitedCompressed;
  DWORD dwPortBytesRcvedCompressed;
} RAS_PORT_STATISTICS, *PRAS_PORT_STATISTICS;
```



## <a name="members"></a>成員

<dl> <dt>

**dwBytesXmited**
</dt> <dd>

指定連接所傳送的位元組總數。

</dd> <dt>

**dwBytesRcved**
</dt> <dd>

指定連接接收的位元組總數。

</dd> <dt>

**dwFramesXmited**
</dt> <dd>

指定連接所傳輸的總畫面數。

</dd> <dt>

**dwFramesRcved**
</dt> <dd>

指定連接接收的總畫面數。

</dd> <dt>

**dwCrcErr**
</dt> <dd>

指定連接上的 CRC 錯誤總數。 CRC 錯誤是因為迴圈冗余檢查失敗所造成。 CRC 錯誤表示收到的資料封包中有一或多個字元在抵達時發現混淆。

</dd> <dt>

**dwTimeoutErr**
</dt> <dd>

指定連接上的逾時錯誤總數。 未及時收到預期的字元時，就會發生逾時錯誤。 發生這種情況時，軟體會假設資料已遺失，並要求重新傳送。

</dd> <dt>

**dwAlignmentErr**
</dt> <dd>

指定連接上的對齊錯誤總數。 當收到的字元不是預期的字元時，就會發生對齊錯誤。 這通常發生于遺失字元或發生逾時錯誤時。

</dd> <dt>

**dwHardwareOverrunErr**
</dt> <dd>

指定連接上的硬體溢出錯誤總數。 這些錯誤指出傳送的電腦傳輸字元的速度，比接收的電腦硬體可以處理更快的次數。 如果此問題持續發生，請降低用戶端的 BPS 連線速度。

</dd> <dt>

**dwFramingErr**
</dt> <dd>

指定連接上的框架錯誤總數。 收到具有無效開始或停止位的非同步字元時，就會發生框架錯誤。

</dd> <dt>

**dwBufferOverrunErr**
</dt> <dd>

指定連接上的緩衝區溢位錯誤總數。 當傳送的電腦傳輸字元的速度比接收電腦可以容納這些字元時，就會發生緩衝區溢位錯誤。 如果此問題持續發生，請降低用戶端的 BPS 連線速度。

</dd> <dt>

**dwBytesXmitedUncompressed**
</dt> <dd>

指定連接未壓縮的位元組總數。

</dd> <dt>

**dwBytesRcvedUncompressed**
</dt> <dd>

指定連接所接收的未壓縮位元組總數。

</dd> <dt>

**dwBytesXmitedCompressed**
</dt> <dd>

指定連接壓縮的總位元組數。

</dd> <dt>

**dwBytesRcvedCompressed**
</dt> <dd>

指定連接已壓縮的位元組總數。

</dd> <dt>

**dwPortBytesXmited**
</dt> <dd>

指定埠傳送的位元組總數。

</dd> <dt>

**dwPortBytesRcved**
</dt> <dd>

指定埠所接收的位元組總數。

</dd> <dt>

**dwPortFramesXmited**
</dt> <dd>

指定埠所傳輸的總畫面數。

</dd> <dt>

**dwPortFramesRcved**
</dt> <dd>

指定埠所接收的總畫面數。

</dd> <dt>

**dwPortCrcErr**
</dt> <dd>

指定埠上的 CRC 錯誤總數。 CRC 錯誤是因為迴圈冗余檢查失敗所造成。 CRC 錯誤表示收到的資料封包中有一或多個字元在抵達時發現混淆。

</dd> <dt>

**dwPortTimeoutErr**
</dt> <dd>

指定埠上的逾時錯誤總數。 未及時收到預期的字元時，就會發生逾時錯誤。 發生這種情況時，軟體會假設資料已遺失，並要求重新傳送。

</dd> <dt>

**dwPortAlignmentErr**
</dt> <dd>

指定埠上的對齊錯誤總數。 當收到的字元不是預期的字元時，就會發生對齊錯誤。 這通常發生于遺失字元或發生逾時錯誤時。

</dd> <dt>

**dwPortHardwareOverrunErr**
</dt> <dd>

指定埠上的硬體溢出錯誤總數。 這些錯誤指出傳送的電腦傳輸字元的速度，比接收的電腦硬體可以處理更快的次數。 如果此問題持續發生，請降低用戶端的 BPS 連線速度。

</dd> <dt>

**dwPortFramingErr**
</dt> <dd>

指定埠上的框架錯誤總數。 收到具有無效開始或停止位的非同步字元時，就會發生框架錯誤。

</dd> <dt>

**dwPortBufferOverrunErr**
</dt> <dd>

指定埠上的緩衝區溢位錯誤總數。 當傳送的電腦傳輸字元的速度比接收電腦可以容納這些字元時，就會發生緩衝區溢位錯誤。 如果此問題持續發生，請降低用戶端的 BPS 連線速度。

</dd> <dt>

**dwPortBytesXmitedUncompressed**
</dt> <dd>

指定埠未壓縮的總位元組數。 如果埠是多重連結連接的一部分，此成員就無效。 請改用連接的壓縮統計資料。

</dd> <dt>

**dwPortBytesRcvedUncompressed**
</dt> <dd>

指定埠未壓縮的總位元組數。 如果埠是多重連結連接的一部分，此成員就無效。 請改用連接的壓縮統計資料。

</dd> <dt>

**dwPortBytesXmitedCompressed**
</dt> <dd>

指定埠所壓縮的總位元組數。 如果埠是多重連結連接的一部分，此成員就無效。 請改用連接的壓縮統計資料。

</dd> <dt>

**dwPortBytesRcvedCompressed**
</dt> <dd>

指定埠已壓縮的位元組總數。 如果埠是多重連結連接的一部分，此成員就無效。 請改用連接的壓縮統計資料。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Rassapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[遠端存取服務 (RAS) 總覽](about-remote-access-service.md)
</dt> <dt>

[RAS 伺服器管理結構](ras-server-administration-structures.md)
</dt> <dt>

[**RAS \_ 埠 \_ 0**](ras-port-0-str.md)
</dt> <dt>

[**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)
</dt> <dt>

[**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md)
</dt> <dt>

[**RasAdminPortClearStatistics**](rasadminportclearstatistics.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





