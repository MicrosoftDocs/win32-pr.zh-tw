---
description: SetKeepAliveInterval WMI 類別靜態方法可用來設定間隔，以分隔保持運作的重新傳輸，直到收到回應為止。
ms.assetid: 83415000-124a-44a7-93cc-92ce9df143aa
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 SetKeepAliveInterval 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetKeepAliveInterval
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5ca52cbc68c834d5216920334763d4de5c982702b8cc562db88ceed7b6de0f12
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759768"
---
# <a name="setkeepaliveinterval-method-of-the-win32_networkadapterconfiguration-class"></a>Win32 >networkadapterconfiguration 類別的 SetKeepAliveInterval 方法 \_

**SetKeepAliveInterval** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)靜態方法可用來設定間隔，以分隔保持運作的重新傳輸，直到收到回應為止。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 SetKeepAliveInterval(
  [in] uint32 KeepAliveInterval
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*KeepAliveInterval* \[在\]
</dt> <dd>

以毫秒為單位的值，以毫秒為單位分隔保持運作的重新傳輸，直到收到回應為止。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，而如果發生錯誤，則為不同的數位。 如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

<dl> <dt>

**成功完成，不需要重新開機**
</dt> <dd>

0

成功完成，不需要重新開機。

</dd> <dt>

**成功完成，需要重新開機**
</dt> <dd>

1

成功完成，需要重新開機。

</dd> <dt>

**此平臺不支援的方法**
</dt> <dd>

64

此平臺不支援方法。

</dd> <dt>

**未知的失敗**
</dt> <dd>

65

未知的失敗。

</dd> <dt>

**不正確子網路遮罩**
</dt> <dd>

66

不正確子網路遮罩。

</dd> <dt>

**處理傳回的實例時發生錯誤**
</dt> <dd>

67

處理傳回的實例時發生錯誤。

</dd> <dt>

**不正確輸入參數**
</dt> <dd>

68

不正確輸入參數。

</dd> <dt>

**指定了超過5個閘道**
</dt> <dd>

69

指定了五個以上的閘道。

</dd> <dt>

**不正確 IP 位址**
</dt> <dd>

70

IP 位址無效。

</dd> <dt>

**閘道 IP 位址無效**
</dt> <dd>

71

閘道 IP 位址無效。

</dd> <dt>

**存取所要求資訊的登錄時發生錯誤**
</dt> <dd>

72

存取所要求資訊的登錄時發生錯誤。

</dd> <dt>

**不正確功能變數名稱**
</dt> <dd>

73

功能變數名稱無效。

</dd> <dt>

**不正確主機名稱**
</dt> <dd>

74

不正確主機名稱。

</dd> <dt>

**未定義主要/次要 WINS 伺服器**
</dt> <dd>

75

未定義主要或次要 WINS 伺服器。

</dd> <dt>

**檔案無效**
</dt> <dd>

76

檔案無效。

</dd> <dt>

**系統路徑無效**
</dt> <dd>

77

不正確系統路徑。

</dd> <dt>

**檔案複製失敗**
</dt> <dd>

78

檔案複製失敗。

</dd> <dt>

**不正確安全性參數**
</dt> <dd>

79

不正確安全性參數。

</dd> <dt>

**無法設定 TCP/IP 服務**
</dt> <dd>

80

無法設定 TCP/IP 服務。

</dd> <dt>

**無法設定 DHCP 服務**
</dt> <dd>

81

無法設定 DHCP 服務。

</dd> <dt>

**無法更新 DHCP 租用**
</dt> <dd>

82

無法更新 DHCP 租用。

</dd> <dt>

**無法發行 DHCP 租用**
</dt> <dd>

83

無法釋放 DHCP 租用。

</dd> <dt>

**介面卡上未啟用 IP**
</dt> <dd>

84

介面卡上未啟用 IP。

</dd> <dt>

**未在介面卡上啟用 IPX**
</dt> <dd>

85

未在介面卡上啟用 IPX。

</dd> <dt>

**畫面格/網路編號界限錯誤**
</dt> <dd>

86

畫面格或網路編號界限錯誤。

</dd> <dt>

**不正確框架類型**
</dt> <dd>

87

不正確畫面格類型。

</dd> <dt>

**不正確網路編號**
</dt> <dd>

88

網路編號無效。

</dd> <dt>

**重複的網路編號**
</dt> <dd>

89

網路編號重複。

</dd> <dt>

**參數超出範圍**
</dt> <dd>

90

參數超出範圍。

</dd> <dt>

**拒絕存取**
</dt> <dd>

91

拒絕存取。

</dd> <dt>

**記憶體不足**
</dt> <dd>

92

記憶體不足。

</dd> <dt>

**已經存在**
</dt> <dd>

93

已經存在。

</dd> <dt>

**找不到路徑、檔案或物件**
</dt> <dd>

94

找不到路徑、檔案或物件。

</dd> <dt>

**無法通知服務**
</dt> <dd>

95

無法通知服務。

</dd> <dt>

**無法通知 DNS 服務**
</dt> <dd>

96

無法通知 DNS 服務。

</dd> <dt>

**介面無法設定**
</dt> <dd>

97

介面無法設定。

</dd> <dt>

**並非所有 DHCP 租用都可以釋出/更新**
</dt> <dd>

98

並非所有 DHCP 租用都可以釋出或更新。

</dd> <dt>

**未在介面卡上啟用 DHCP**
</dt> <dd>

100

未在介面卡上啟用 DHCP。

</dd> <dt>

**其他**
</dt> <dd>

101 4294967295

</dd> </dl>

## <a name="remarks"></a>備註

收到回應之後，會延遲到下一個保持運作的傳輸，再由 [**KeepAliveTime**](win32-networkadapterconfiguration.md) 屬性的值來控制。 在 **TcpMaxDataRetransmissions** 屬性所指定的重新傳輸數目未接聽之後，連接會終止

## <a name="examples"></a>範例

[ [修改所有網路介面卡的保持運作間隔](https://Gallery.TechNet.Microsoft.Com/f6d4a0e7-5b59-42e3-888d-82a028e2bf35) ] VBScript 範例會將電腦上所有網路介面卡的保持運作間隔設定為300、00毫秒 (5 分鐘的) 。

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

[電腦系統硬體類別](computer-system-hardware-classes.md)
</dt> <dt>

[**Win32 \_ >networkadapterconfiguration**](win32-networkadapterconfiguration.md)
</dt> <dt>

[WMI 工作：網路功能](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[WMI 工作：帳戶和網域](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[WMI 中的 IPv6 和 IPv4 支援](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

