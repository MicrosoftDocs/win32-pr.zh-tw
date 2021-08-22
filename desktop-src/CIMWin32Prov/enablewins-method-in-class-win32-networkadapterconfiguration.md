---
description: '>enablewins &\# 32;WMI 類別靜態方法會啟用 Windows 的網際網路命名服務 (tcp/ip 的 WINS) 設定，但與網路介面卡無關。'
ms.assetid: ce0fb170-978f-4d70-bced-e530e43da719
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 >enablewins 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableWINS
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ce820e515bb72cbd2521521726f2b6962c49ee1b453781b5d17993c45e0d22d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118676501"
---
# <a name="enablewins-method-of-the-win32_networkadapterconfiguration-class"></a>Win32 >networkadapterconfiguration 類別的 >enablewins 方法 \_

**>enablewins** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)靜態方法會啟用 Windows 的網際網路命名服務 (tcp/ip 的 WINS) 設定，但與網路介面卡無關。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 EnableWINS(
  [in]           boolean DNSEnabledForWINSResolution,
  [in]           boolean WINSEnableLMHostsLookup,
  [in, optional] string  WINSHostLookupFile,
  [in, optional] string  WINSScopeID
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*DNSEnabledForWINSResolution* \[在\]
</dt> <dd>

若 **為 true**，則會啟用網域名稱系統 (DNS) ，以透過 WINS 解析進行名稱解析。

</dd> <dt>

*WINSEnableLMHostsLookup* \[在\]
</dt> <dd>

若 **為 true**，則會使用本機查閱檔案。 查閱檔案將包含 IP 位址與主機名稱的對應。

</dd> <dt>

*WINSHostLookupFile* \[在中，選擇性\]
</dt> <dd>

查閱檔案，其中包含 IP 位址與主機名稱的對應。 如果有的話，檔案會在% SystemRoot% \\ system32 \\ 驅動程式中找到 \\ 。

</dd> <dt>

*WINSScopeID* \[在中，選擇性\]
</dt> <dd>

將附加至電腦 NetBIOS 名稱結尾的範圍識別碼值。 使用相同範圍識別碼的系統可以與這部電腦通訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值為 0 (零) 表示在不需要重新開機時成功完成;1 (需要重新開機時，成功完成的一) ;如果發生錯誤，則為不同的數位。 如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

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

## <a name="examples"></a>範例

TechNet 資源庫上的「 [啟用所有網路介面卡的 wins](https://Gallery.TechNet.Microsoft.Com/64cae6dd-4155-4825-ab25-5727503edf5a) 」 VBScript 程式碼範例會使用 **>enablewins** ，在電腦上安裝的所有網路介面卡上啟用 wins。

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

 

