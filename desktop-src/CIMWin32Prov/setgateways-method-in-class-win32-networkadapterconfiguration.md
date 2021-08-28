---
description: SetGateways &\# 32;WMI 類別方法會指定閘道清單，以將封包路由傳送至與網路介面卡所連線之子網不同的子網。
ms.assetid: 240f7aff-7a07-4e0d-af30-7bcabb68c736
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 SetGateways 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetGateways
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 190076822a181d7b0731cb1e7b42eb0cd9d35e37c64aa0736245d1e58994763b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759718"
---
# <a name="setgateways-method-of-the-win32_networkadapterconfiguration-class"></a>Win32 >networkadapterconfiguration 類別的 SetGateways 方法 \_

**SetGateways** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會指定閘道清單，以將封包路由傳送至與網路介面卡所連線之子網不同的子網。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 SetGateways(
  [in]           string DefaultIPGateway[],
  [in, optional] uint16 GatewayCostMetric[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*DefaultIPGateway* \[在\]
</dt> <dd>

路由傳送網路封包之閘道的 IP 位址清單。

</dd> <dt>

*GatewayCostMetric* \[在中，選擇性\]
</dt> <dd>

指派範圍從1到9999的值，用來計算最快且最可靠的路由。 此參數的值會對應到 *DefaultIPGateway* 參數中的值。 閘道的預設值為1。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果不需要重新開機，則傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，以及任何其他值（如果發生錯誤）。 如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

<dl> <dt>

**成功完成，不需要重新開機**
</dt> <dd>

0

</dd> <dt>

**成功完成，需要重新開機**
</dt> <dd>

1

</dd> <dt>

**此平臺不支援的方法**
</dt> <dd>

64

當 NIC 處於 DHCP 模式時不支援的方法。

</dd> <dt>

**未知的失敗**
</dt> <dd>

65

</dd> <dt>

**不正確子網路遮罩**
</dt> <dd>

66

</dd> <dt>

**處理傳回的實例時發生錯誤**
</dt> <dd>

67

</dd> <dt>

**不正確輸入參數**
</dt> <dd>

68

</dd> <dt>

**指定了超過5個閘道**
</dt> <dd>

69

</dd> <dt>

**不正確 IP 位址**
</dt> <dd>

70

</dd> <dt>

**閘道 IP 位址無效**
</dt> <dd>

71

</dd> <dt>

**存取所要求資訊的登錄時發生錯誤**
</dt> <dd>

72

</dd> <dt>

**不正確功能變數名稱**
</dt> <dd>

73

</dd> <dt>

**不正確主機名稱**
</dt> <dd>

74

</dd> <dt>

**未定義主要/次要 WINS 伺服器**
</dt> <dd>

75

</dd> <dt>

**檔案無效**
</dt> <dd>

76

</dd> <dt>

**系統路徑無效**
</dt> <dd>

77

</dd> <dt>

**檔案複製失敗**
</dt> <dd>

78

</dd> <dt>

**不正確安全性參數**
</dt> <dd>

79

</dd> <dt>

**無法設定 TCP/IP 服務**
</dt> <dd>

80

</dd> <dt>

**無法設定 DHCP 服務**
</dt> <dd>

81

</dd> <dt>

**無法更新 DHCP 租用**
</dt> <dd>

82

</dd> <dt>

**無法發行 DHCP 租用**
</dt> <dd>

83

</dd> <dt>

**介面卡上未啟用 IP**
</dt> <dd>

84

</dd> <dt>

**未在介面卡上啟用 IPX**
</dt> <dd>

85

</dd> <dt>

**畫面格/網路編號界限錯誤**
</dt> <dd>

86

</dd> <dt>

**不正確框架類型**
</dt> <dd>

87

</dd> <dt>

**不正確網路編號**
</dt> <dd>

88

</dd> <dt>

**重複的網路編號**
</dt> <dd>

89

</dd> <dt>

**參數超出範圍**
</dt> <dd>

90

</dd> <dt>

**拒絕存取**
</dt> <dd>

91

</dd> <dt>

**記憶體不足**
</dt> <dd>

92

</dd> <dt>

**已經存在**
</dt> <dd>

93

</dd> <dt>

**找不到路徑、檔案或物件**
</dt> <dd>

94

</dd> <dt>

**無法通知服務**
</dt> <dd>

95

</dd> <dt>

**無法通知 DNS 服務**
</dt> <dd>

96

</dd> <dt>

**介面無法設定**
</dt> <dd>

97

</dd> <dt>

**並非所有 DHCP 租用都可以釋出/更新**
</dt> <dd>

98

</dd> <dt>

**未在介面卡上啟用 DHCP**
</dt> <dd>

100

</dd> <dt>

**其他**
</dt> <dd>

101 4294967295

</dd> </dl>

## <a name="remarks"></a>備註

只有當網路介面卡 (NIC) 處於靜態 IP 模式時，此方法才會運作。

若要清除閘道，請將您的閘道設定為您在 [**EnableStatic**](enablestatic-method-in-class-win32-networkadapterconfiguration.md)上使用的相同 IP。

## <a name="examples"></a>範例

[修改網路介面卡](https://Gallery.TechNet.Microsoft.Com/9ea7670b-f68f-4efb-9cd2-7c299a8f657f)VBScript 範例的閘道會針對網路介面卡設定兩個閘道。

[指派靜態 IP 位址](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a)VBScript 範例會設定電腦的 IP 位址和閘道。

[靜態 IP 然後加入網域](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a)PowerShell 範例可協助重建電腦。

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

 

