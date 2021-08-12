---
title: 'IVMGuestOS IsHeartbeating 屬性 (VPCCOMInterfaces .h) '
description: 判斷虛擬機器是否有信號。
ms.assetid: b1697a7b-6119-47aa-b261-6009f5287993
keywords:
- IsHeartbeating 屬性 Virtual PC
- IsHeartbeating 屬性 Virtual PC，IVMGuestOS 介面
- IVMGuestOS 介面 Virtual PC，IsHeartbeating 屬性
topic_type:
- apiref
api_name:
- IVMGuestOS.IsHeartbeating
- IVMGuestOS.get_IsHeartbeating
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91598284d3765c5ff6de185ca0cf3b652036c226d80b0fe01a9944a9d7480b43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118594178"
---
# <a name="ivmguestosisheartbeating-property"></a>IVMGuestOS：： IsHeartbeating 屬性

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

判斷虛擬機器是否有信號。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_IsHeartbeating(
  [out, retval] VARIANT_BOOL *heartBeating
);
```



## <a name="property-value"></a>屬性值

**變異 \_** 如果偵測到信號，則為 TRUE，否則為 **VARIANT \_** 。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                              | 意義                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                                 | 作業成功。<br/>                                                                                                                         |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>                   | 參數為 **Null**。<br/>                                                                                                                            |
| <dl> <dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt> </dl>           | 未知的設定。<br/>                                                                                                                         |
| <dl> <dt>VM \_E \_ VM \_ 未 \_ </dt>執行 <dt>0xA0040206</dt> </dl>      | 虛擬機器必須正在執行，才能進行這種操作。<br/>                                                                                               |
| <dl> <dt>VM \_E \_ 新增 \_ 專案 \_ 無法</dt> <dt>0xA0040504</dt> </dl> | 虛擬機器未完全啟動、未安裝整合元件功能，或安裝的版本不支援此功能。<br/> |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>           | 已發生未預期的錯誤。<br/>                                                                                                                     |



## <a name="remarks"></a>備註

當整合元件安裝在客體作業系統時，系統會將標準的「滴答」或心跳從虛擬機器會話傳送到 Windows virtual PC。 如果虛擬電腦的負載很高，則虛擬電腦可能會收到比預期更少的心跳。 如果未偵測到任何偵測到的偵測，則可能是客體作業系統沒有回應或損毀。

根據預設，虛擬機器每分鐘會產生10個信號刻度。 如果未偵測到整分鐘的任何心跳滴答，Windows virtual PC 會每十秒嘗試重新開機虛擬機器會話一次，最多兩分鐘。 此行為是由虛擬機器會話設定檔中的下列索引鍵值所控制。



| 組態機碼                                            | 預設       | 描述                                                                                                                             |
|--------------------------------------------------------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| 整合/microsoft/心跳/時間<br/>              | 60<br/> | 用來產生信號刻度的時間區塊長度（以秒為單位）。<br/>                                             |
| 整合/microsoft/心跳/比率<br/>              | 10<br/> | 每個信號時間區塊中產生的刻度數目。<br/>                                                                  |
| 整合/microsoft/信號/失敗 \_ 間隔<br/> | 10<br/> | 在特定的時間區塊內未收到任何心跳滴答之後，重新開機嘗試之間的秒數。<br/> |
| 整合/microsoft/信號/失敗 \_ 嘗試<br/> | 12<br/> | 嘗試重新開機的次數。<br/>                                                                                         |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS 定義為99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

