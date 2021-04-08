---
description: SetDNSServerSearchOrder &\# 32;WMI 類別方法會使用 string 元素陣列來設定伺服器搜尋順序。
ms.assetid: fce688fa-7264-4965-8e1c-138160e03a7e
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 SetDNSServerSearchOrder 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDNSServerSearchOrder
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2bfe731ea1d89e8e0ad702bfa229a61fba30dfc7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025960"
---
# <a name="setdnsserversearchorder-method-of-the-win32_networkadapterconfiguration-class"></a>Win32 >networkadapterconfiguration 類別的 SetDNSServerSearchOrder 方法 \_

**SetDNSServerSearchOrder** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會使用 string 元素陣列來設定伺服器搜尋順序。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 SetDNSServerSearchOrder(
  [in] string DNSServerSearchOrder[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*DNSServerSearchOrder* \[在\]
</dt> <dd>

要查詢 DNS 伺服器的伺服器 IP 位址清單。

範例：130.215.24.1 或157.54.164。1

</dd> </dl>

## <a name="return-value"></a>傳回值

如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，而如果發生錯誤，則為不同的數位。 如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

<dl> <dt>

**成功完成，不需要重新開機** (0) 
</dt> <dt>

**成功完成，需要重新開機** (1) 
</dt> <dt>

**此平臺 (64) 不支援的方法**
</dt> <dt>

**未知的失敗** (65) 
</dt> <dt>

**不正確子網路遮罩** (66) 
</dt> <dt>

**處理傳回的實例時發生錯誤** (67) 
</dt> <dt>

**不正確輸入參數** (68) 
</dt> <dt>

 (69) **指定超過5個閘道**
</dt> <dt>

**不正確 IP 位址** (70) 
</dt> <dt>

**不正確閘道 IP 位址** (71) 
</dt> <dt>

**存取所要求資訊** 的登錄時發生錯誤 (72) 
</dt> <dt>

**不正確功能變數名稱** (73) 
</dt> <dt>

**不正確主機名稱** (74) 
</dt> <dt>

**未定義任何主要/次要 WINS 伺服器** (75) 
</dt> <dt>

**不正確檔** (76) 
</dt> <dt>

**不正確系統路徑** (77) 
</dt> <dt>

檔案 **複製失敗** (78) 
</dt> <dt>

 (79) 的 **安全性參數無效**
</dt> <dt>

**無法設定 tcp/ip 服務** (80) 
</dt> <dt>

**無法設定 DHCP 服務** (81) 
</dt> <dt>

**無法更新 DHCP 租用** (82) 
</dt> <dt>

**無法釋放 DHCP 租用** (83) 
</dt> <dt>

**介面卡上未啟用 IP** (84) 
</dt> <dt>

**未在介面卡上啟用 IPX** (85) 
</dt> <dt>

**畫面格/網路編號界限錯誤** (86) 
</dt> <dt>

**不正確框架類型** (87) 
</dt> <dt>

 (88) 的 **網路編號無效**
</dt> <dt>

 (89) **重複的網路編號**
</dt> <dt>

**參數超出範圍** (90) 
</dt> <dt>

**拒絕存取** (91) 
</dt> <dt>

**記憶體不足** (92) 
</dt> <dt>

**已存在** (93) 
</dt> <dt>

**找不到路徑、檔案或物件** (94) 
</dt> <dt>

**無法通知服務** (95) 
</dt> <dt>

**無法通知 DNS 服務** (96) 
</dt> <dt>

**介面無法** 設定 (97) 
</dt> <dt>

**並非所有 DHCP 租用都** 可以釋出/更新 (98) 
</dt> <dt>

**未在介面卡上啟用 DHCP** (100) 
</dt> <dt>

**其他** (101 4294967295) 
</dt> </dl>

## <a name="remarks"></a>備註

這是每個介面卡上套用的實例相依方法呼叫。 指定靜態 DNS 伺服器來開始使用動態主機設定通訊協定 (DHCP) 而不是靜態 DNS 伺服器，您可以呼叫方法，而不需提供 "in" 參數。

## <a name="examples"></a>範例

TechNet 資源庫上的 [多部電腦在組織單位的 VBScript 範例中設定 Dns 伺服器搜尋順序](https://Gallery.TechNet.Microsoft.Com/Set-DNS-Server-Search-6a3e3ede) ，可針對屬於一個組織單位的多部電腦，取得或設定 dns 伺服器搜尋順序。

「 [修改網路介面卡的 DNS 伺服器搜尋順序](https://Gallery.TechNet.Microsoft.Com/7824348c-5a92-42cb-b4e9-ef2187702e02) 」 VBScript 範例會設定 tcp/ip 系結的網路介面卡，以使用兩部 DNS 伺服器。

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

 

