---
description: 為此網路介面卡設定網路封包 Exchange (IPX) 網路編號/畫面格配對。
ms.assetid: 8190564f-7d9f-4b05-9949-2e732ce36dba
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 SetIPXFrameTypeNetworkPairs 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPXFrameTypeNetworkPairs
api_type:
- COM
api_location:
- cimwin32.dll
ms.openlocfilehash: f914f996e26d64ae66c0be2acf1dee3988ccc2015109c6e7d3b340b406c0c23e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973020"
---
# <a name="setipxframetypenetworkpairs-method-of-the-win32_networkadapterconfiguration-class"></a>Win32 >networkadapterconfiguration 類別的 SetIPXFrameTypeNetworkPairs 方法 \_

為此網路介面卡設定網路封包 Exchange (IPX) 網路編號/畫面格配對。

Windows 2000 和 Windows NT 3.51 和更新版本會使用 IPX 網路編號來進行路由。 它會指派給電腦系統上每個設定的畫面格類型/網路介面卡組合。 此數位有時稱為「外部網路編號」。 對於每個網路區段而言，它必須是唯一的。 如果畫面類型設定為 [自動]，則網路編號應為零。

## <a name="syntax"></a>語法


```mof
uint32 SetIPXFrameTypeNetworkPairs(
  [in] string IPXNetworkNumber[],
  [in] uint32 IPXFrameType[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*IPXNetworkNumber* \[在\]
</dt> <dd>

字元陣列，可唯一識別電腦系統上的介面卡。 NetWare 連結 (NWLink) Windows 2000 和 Windows NT 3.51 或更高版本中的 IPX/SPX 相容傳輸，會使用兩種不同類型的網路編號。 此數位有時稱為外部網路編號。 對於每個網路區段而言，它必須是唯一的。 此字串清單中的值必須在 IPXFrameType 參數中有對應的值，以識別用於此網路的封包框架類型。

</dd> <dt>

*IPXFrameType* \[在\]
</dt> <dd>

框架類型識別碼的整數陣列。 這個陣列中的值會對應到 *IPXNetworkNumber* 參數中的元素。

<dt>

<span id="Ethernet_II"></span><span id="ethernet_ii"></span><span id="ETHERNET_II"></span>

**ETHERNET II** (0) 


</dt> <dd></dd> <dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

**Ethernet 802.3** (1) 


</dt> <dd></dd> <dt>

<span id="Ethernet_802.2"></span><span id="ethernet_802.2"></span><span id="ETHERNET_802.2"></span>

**Ethernet 802.2** (2) 


</dt> <dd></dd> <dt>

<span id="Ethernet_SNAP"></span><span id="ethernet_snap"></span><span id="ETHERNET_SNAP"></span>

**Ethernet 貼齊** (3) 


</dt> <dd></dd> <dt>

<span id="AUTO"></span><span id="auto"></span>

**自動** (255) 


</dt> <dd></dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

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

**其他** (101 – 4294967295) 
</dt> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CimWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Cimwin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ >networkadapterconfiguration**](win32-networkadapterconfiguration.md)
</dt> </dl>

 

 




