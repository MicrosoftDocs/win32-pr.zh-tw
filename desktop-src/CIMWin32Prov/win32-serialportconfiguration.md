---
description: Win32 \_ SERIALPORTCONFIGURATION WMI 類別代表以 Windows 為基礎之序列埠上的資料傳輸設定。 這包括建立連接和錯誤檢查的設定。
ms.assetid: 688cdcce-8325-4b4d-93ab-5a602e9e3f8e
ms.tgt_platform: multiple
title: Win32_SerialPortConfiguration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPortConfiguration
- Win32_SerialPortConfiguration.Caption
- Win32_SerialPortConfiguration.Description
- Win32_SerialPortConfiguration.SettingID
- Win32_SerialPortConfiguration.AbortReadWriteOnError
- Win32_SerialPortConfiguration.BaudRate
- Win32_SerialPortConfiguration.BinaryModeEnabled
- Win32_SerialPortConfiguration.BitsPerByte
- Win32_SerialPortConfiguration.ContinueXMitOnXOff
- Win32_SerialPortConfiguration.CTSOutflowControl
- Win32_SerialPortConfiguration.DiscardNULLBytes
- Win32_SerialPortConfiguration.DSROutflowControl
- Win32_SerialPortConfiguration.DSRSensitivity
- Win32_SerialPortConfiguration.DTRFlowControlType
- Win32_SerialPortConfiguration.EOFCharacter
- Win32_SerialPortConfiguration.ErrorReplaceCharacter
- Win32_SerialPortConfiguration.ErrorReplacementEnabled
- Win32_SerialPortConfiguration.EventCharacter
- Win32_SerialPortConfiguration.IsBusy
- Win32_SerialPortConfiguration.Name
- Win32_SerialPortConfiguration.Parity
- Win32_SerialPortConfiguration.ParityCheckEnabled
- Win32_SerialPortConfiguration.RTSFlowControlType
- Win32_SerialPortConfiguration.StopBits
- Win32_SerialPortConfiguration.XOffCharacter
- Win32_SerialPortConfiguration.XOffXMitThreshold
- Win32_SerialPortConfiguration.XOnCharacter
- Win32_SerialPortConfiguration.XOnXMitThreshold
- Win32_SerialPortConfiguration.XOnXOffInFlowControl
- Win32_SerialPortConfiguration.XOnXOffOutFlowControl
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 065d069b261472e3347a115cfbbff652812b6622
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936109"
---
# <a name="win32_serialportconfiguration-class"></a>Win32 \_ SerialPortConfiguration 類別

**Win32 \_ SerialPortConfiguration** [WMI 類別](../wmisdk/retrieving-a-class.md)代表以 Windows 為基礎之序列埠上的資料傳輸設定。 這包括建立連接和錯誤檢查的設定。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPortConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  boolean AbortReadWriteOnError;
  uint32  BaudRate;
  boolean BinaryModeEnabled;
  uint32  BitsPerByte;
  boolean ContinueXMitOnXOff;
  boolean CTSOutflowControl;
  boolean DiscardNULLBytes;
  boolean DSROutflowControl;
  boolean DSRSensitivity;
  string  DTRFlowControlType;
  uint32  EOFCharacter;
  uint32  ErrorReplaceCharacter;
  boolean ErrorReplacementEnabled;
  uint32  EventCharacter;
  boolean IsBusy;
  string  Name;
  string  Parity;
  boolean ParityCheckEnabled;
  string  RTSFlowControlType;
  string  StopBits;
  uint32  XOffCharacter;
  uint32  XOffXMitThreshold;
  uint32  XOnCharacter;
  uint32  XOnXMitThreshold;
  uint32  XOnXOffInFlowControl;
  uint32  XOnXOffOutFlowControl;
};
```

## <a name="members"></a>成員

**Win32 \_ SerialPortConfiguration** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ SerialPortConfiguration** 類別具有這些屬性。

<dl> <dt>

**AbortReadWriteOnError**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fAbortOnError" ) 
</dt> </dl>

若 **為 TRUE**，則會在發生錯誤時終止讀取和寫入作業。 若 **為 TRUE**，當發生錯誤時，驅動程式會終止所有的讀取和寫入作業，並顯示錯誤狀態。 在應用程式確認錯誤之前，驅動程式將不會接受任何進一步的通訊作業。

</dd> <dt>

**串列傳輸速率**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| 串列傳輸速率" ) 
</dt> </dl>

每秒傳輸 (位數) 通訊裝置運作的速率。

範例：9600

</dd> <dt>

**BinaryModeEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fBinary" ) 
</dt> </dl>

若 **為 TRUE**，則會啟用序列埠的二進位模式資料傳輸。 執行 Windows 的電腦系統只允許透過序列埠進行二進位傳輸，因此這個值一律 **為 TRUE**。

</dd> <dt>

**BitsPerByte**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ByteSize" ) 
</dt> </dl>

Windows 序列埠的每個位元組資料傳輸和接收的位元組數目。 此數目可能會隨著控制項和錯誤更正位（例如同位檢查位）而有所不同。

範例：8

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) 
</dt> </dl>

目前物件的簡短文字描述。

這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。

</dd> <dt>

**ContinueXMitOnXOff**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fTXContinueOnXoff" ) 
</dt> </dl>

若 **為 TRUE**，當輸入緩衝區在 **XOffXMitThreshold** 個位元組內已滿，且驅動程式已傳送 **XOffChararcter** 值以停止接收位元組時，資料傳輸會繼續。 若 **為 FALSE**，則在輸入緩衝區在 **XOnXMitThreshold** 個位元組內為空白且驅動程式已傳送 **XOnCharacter** 值以繼續接收之前，傳輸將無法繼續。

</dd> <dt>

**CTSOutflowControl**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutxCtsFlow" ) 
</dt> </dl>

若為 **TRUE**，則會在傳輸資料之前，先檢查要傳送 (CTS 的 clear) 信號。 CTS 表示序列連接上的兩部裝置都已準備好傳輸資料。 資料傳輸會暫止，直到獲得 CTS 信號為止。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

目前物件的文字描述。

這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。

</dd> <dt>

**DiscardNullBytes**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fNull" ) 
</dt> </dl>

若 **為 TRUE**，則會在收到 **Null** 位元組後將其捨棄 (的字元) 。

</dd> <dt>

**DSROutflowControl**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutxDsrFlow" ) 
</dt> </dl>

若為 **TRUE**，當資料集就緒 (DSR) 條件時，便會啟用資料流程控制。 DSR 表示連接已由序列連接上的裝置所建立。 DSR 資料傳輸會暫止，直到指定 DSR 信號為止。

</dd> <dt>

**DSRSensitivity**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fDsrSensitivity" ) 
</dt> </dl>

若 **為 TRUE**，則表示通訊驅動程式會區分 DSR 信號的狀態。 除非 DSR 數據機輸入行很高，否則驅動程式會忽略任何收到的位元組。

</dd> <dt>

**DTRFlowControlType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fDtrControl" ) 
</dt> </dl>

建立連線之後，使用資料終端機 (DTR) 流量控制。

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

**啟用** ( "enable" ) 


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

**停** 用 ( 「停用」 ) 


</dt> <dd></dd> <dt>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>

**交握** ( 「交握」 ) 


</dt> <dd></dd> </dl>

</dd> <dt>

**EOFCharacter**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| EofChar" ) 
</dt> </dl>

用來表示資料結尾的字元值。

範例： ^ Z

</dd> <dt>

**ErrorReplaceCharacter**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ErrorChar" ) 
</dt> </dl>

用來取代以同位檢查錯誤接收之位元組的字元值。

範例： ^ C

</dd> <dt>

**ErrorReplacementEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fErrorChar" ) 
</dt> </dl>

若 **為 TRUE**，則會以 **ErrorReplaceCharacter** 值取代以同位錯誤接收的位元組。 只有當此屬性為 **TRUE** 且已啟用同位時，才會取代具有同位錯誤的字元。

</dd> <dt>

**EventCharacter**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| EvtChar" ) 
</dt> </dl>

用來通知事件的控制字元值，例如檔案結尾。

範例： ^ e

</dd> <dt>

**System.componentmodel.backgroundworker.isbusy**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| File 函數 \| CreateFile" ) 
</dt> </dl>

若 **為 TRUE**，則表示序列埠忙碌中。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| 硬體 \\ \\ DeviceMap \\ \\ SerialComm" ) 
</dt> </dl>

Windows 序列埠的名稱。

範例： "COM1"

</dd> <dt>

**Parity**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)同位 \| " ) 
</dt> </dl>

要使用的同位檢查方法。 同位是做為錯誤檢查技術，其中每個資料單位都包含額外的同位位。 然後接收者可以藉由計算已設定的位來確認資料的有效性。

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**無** ( 「無」 ) 


</dt> <dd>

未使用同位檢查。

</dd> <dt>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>**奇數** ( 「奇數」 ) 


</dt> <dd>

設定同位檢查位元，以便位元集計數為奇數。

</dd> <dt>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>**甚至** ( 「偶數」 ) 


</dt> <dd>

設定同位檢查位元，以便位元集計數為偶數。

</dd> <dt>

<span id="Mark"></span><span id="mark"></span><span id="MARK"></span>

<span id="Mark"></span><span id="mark"></span><span id="MARK"></span>**標記** ( "mark" ) 


</dt> <dd>

將同位檢查位元集保持為 1。

</dd> <dt>

<span id="Space"></span><span id="space"></span><span id="SPACE"></span>

<span id="Space"></span><span id="space"></span><span id="SPACE"></span>**空間** ( 「空間」 ) 


</dt> <dd>

將同位位設定為 0 (零) 。

</dd> </dl>

</dd> <dt>

**ParityCheckEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fParity" ) 
</dt> </dl>

若 **為 TRUE**，則會啟用同位檢查。

</dd> <dt>

**RTSFlowControlType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

要求傳送 (RTS) 流量控制。 使用 RTS 來指示資料可供傳輸。

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**啟用** ( "enable" ) 


</dt> <dd>

資料傳輸會話的 RTS 會保持開啟。

</dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**停** 用 ( 「停用」 ) 


</dt> <dd>

收到第一個 RTS 信號之後，會忽略 RTS。

</dd> <dt>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>**交握** ( 「交握」 ) 


</dt> <dd>

如果傳輸緩衝區超過三個季滿，則會關閉 RTS，而且當緩衝區小於一半時，會開啟 rts。

</dd> <dt>

<span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>

<span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>**切換** ( "切換" ) 


</dt> <dd>

如果有任何資料緩衝處理以進行傳輸，則會開啟 RTS。

</dd> </dl>

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 
</dt> </dl>

已知目前物件的識別碼。

這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。

</dd> <dt>

**StopBits**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| StopBits" ) 
</dt> </dl>

要使用的停止位數目。 停止位會將非同步序列連接上的每個資料單位分開。 當沒有資料可供傳輸時，也會持續傳送這些資料。

<dt>

<span id="1"></span>

**1** ( "1" ) 


</dt> <dd></dd> <dt>

<span id="1.5"></span>

**1.5** ( "1.5" ) 


</dt> <dd></dd> <dt>

<span id="2"></span>

**2** ( "2" ) 


</dt> <dd></dd> </dl>

</dd> <dt>

**XOffCharacter**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XoffChar" ) 
</dt> </dl>

傳輸和接收的 XOFF 字元值。 XOFF 是用來停止傳輸資料 (的軟體控制項，而 RTS 和 CTS 則是) 的硬體控制項。 XON 會繼續傳輸。

</dd> <dt>

**XOffXMitThreshold**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XoffLim" ) 
</dt> </dl>

傳送 XOFF 字元之前，輸入緩衝區中允許的最大位元組數目。

</dd> <dt>

**XOnCharacter**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XonChar" ) 
</dt> </dl>

用於傳輸和接收的 XON 字元值。 XON 是一種軟體控制，可繼續傳輸資料 (而 RTS 和 CTS 則是) 的硬體控制項。 XOFF 停止傳輸。

</dd> <dt>

**XOnXMitThreshold**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XonLim" ) 
</dt> </dl>

傳送 XON 字元之前，輸入緩衝區中允許的位元組數目下限。 這個屬性會與 **XOffXMitThreshold** 搭配使用，以管制傳輸資料的速率。

</dd> <dt>

**XOnXOffInFlowControl**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fInX" ) 
</dt> </dl>

若 **為 TRUE**，則會在接收期間使用 XON/XOFF 流量控制。 若 **為 TRUE**，當輸入緩衝區進入已滿的 **XOffXMitThreshold** 位元組內時，便會傳送 **XOffCharacter** 值，而且當輸入緩衝區進入空的 **XOnXMitThreshold** 位元組內時，便會傳送 **XOnCharacter** 值。

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

FALSE

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

true

</dd> </dl>

</dd> <dt>

**XOnXOffOutFlowControl**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutX" ) 
</dt> </dl>

**XOnXOffOutFlowControl** 會指定是否在傳輸期間使用 XON 或 XOFF 流量控制。 若 **為 TRUE**，則傳輸會在收到 **XOffCharacter** 值時停止，並在收到 **XOnCharacter** 值時重新開機。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ SerialPortConfiguration** 類別衍生自 [**CIM \_ 設定**](cim-setting.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 設定**](cim-setting.md)
</dt> <dt>

[電腦系統硬體類別](computer-system-hardware-classes.md)
</dt> </dl>

 

 
