---
description: 抓取識別系統上可用之產品套件的位元遮罩。 如果在伺服器接收器內容中執行的應用程式中呼叫此函式，則會改為抓取伺服器定址接收器的套件遮罩。
ms.assetid: 1D6434FD-D7BD-45F9-B7C3-238890AF9928
title: 'RtlGetSuiteMask 函式 (Ntddk) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetSuiteMask
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: c6a71a2cb697021edcf8cea3da8759bbe40aa8ed9be2a93f8adcbeba4197ef88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763467"
---
# <a name="rtlgetsuitemask-function"></a>RtlGetSuiteMask 函式

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

抓取識別系統上可用之產品套件的位元遮罩。 如果在伺服器接收器內容中執行的應用程式中呼叫此函式，則會改為抓取伺服器定址接收器的套件遮罩。

## <a name="syntax"></a>語法


```C++
ULONG NTAPI RtlGetSuiteMask(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

識別系統上可用之產品套件的位元遮罩。 位元遮罩可以包含下列值。



| 傳回值                                                                          | 描述                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl> | Microsoft Small Business Server 已安裝在系統上，但可能已升級至另一個版本的 Windows。 如需此位旗標的詳細資訊，請參閱「備註」一節。<br/>                                           |
| <dl> <dt>0x00000002</dt> </dl> | 已安裝 Windows 10 企業版、Windows 8.1 企業版、Windows Server 2008 Enterprise、Windows Server 2003、Enterprise Edition 或 Windows 2000 Advanced Server。 如需此位旗標的詳細資訊，請參閱「備註」一節。<br/> |
| <dl> <dt>0x00000004</dt> </dl> | 已安裝 Microsoft BackOffice 元件。<br/>                                                                                                                                                                                               |
| <dl> <dt>0x00000008</dt> </dl> | 已安裝通訊伺服器2003、communication Server 2005、communication Server 2007 或 communication Server 2007 R2。<br/>                                                                                                           |
| <dl> <dt>0x00000010</dt> </dl> | 已安裝終端機服務。 一律會設定這個值。<br/> 如果已設定 **TerminalServer** ，但未設定 **SingleUserTS** ，則系統會在應用程式伺服器模式中執行。<br/>                                                         |
| <dl> <dt>0x00000020</dt> </dl> | Microsoft Small Business Server 會以強制的嚴格用戶端授權安裝。 如需此位旗標的詳細資訊，請參閱「備註」一節。<br/>                                                                            |
| <dl> <dt>0x00000040</dt> </dl> | Windows已安裝 XP Embedded。<br/>                                                                                                                                                                                                            |
| <dl> <dt>0x00000080</dt> </dl> | Windows已安裝 server 2008 datacenter、Windows server 2003、datacenter Edition 或 Windows 2000 datacenter Server。<br/>                                                                                                                     |
| <dl> <dt>0x00000100</dt> </dl> | 支援遠端桌面，但只支援一個互動式會話。 除非系統是在應用程式伺服器模式中執行，否則會設定此值。<br/>                                                                                       |
| <dl> <dt>0x00000200</dt> </dl> | Windowsvista home 進階版、Windows vista home Basic 或 Windows XP home Edition 皆已安裝。<br/>                                                                                                                                               |
| <dl> <dt>0x00000400</dt> </dl> | Windows伺服器2003，Web Edition 已安裝。<br/>                                                                                                                                                                                               |
| <dl> <dt>0x00002000</dt> </dl> | 已安裝 Windows 儲存體 server 2003 R2 或 Windows 儲存體 server 2003。<br/>                                                                                                                                                                  |
| <dl> <dt>0x00004000</dt> </dl> | Windows已安裝 Server 2003、Compute Cluster Edition。<br/>                                                                                                                                                                                   |
| <dl> <dt>0x00008000</dt> </dl> | Windows已安裝 Home Server。<br/>                                                                                                                                                                                                            |



 

## <a name="remarks"></a>備註

您不應該只依賴0x00000001 旗標來判斷系統上是否已安裝 Small Business Server，因為此旗標和0x00000020 旗標都是在安裝此產品套件時所設定。 如果您將此安裝升級為 Windows Server，Standard Edition 將會清除0x00000020 旗標，但0x00000001 旗標仍會保持設定。 在此情況下，這表示此系統上已安裝 Small Business Server。 如果此安裝進一步升級為 Windows Server，Enterprise Edition，0x00000001 旗標將保持設定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows Server 2016 \[僅限桌面應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Ntddk。h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Ntdll.dll .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 




