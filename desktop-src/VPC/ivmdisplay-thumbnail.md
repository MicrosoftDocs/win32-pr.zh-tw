---
title: 'IVMDisplay 縮圖屬性 (VPCCOMInterfaces .h) '
description: '抓取圖元的陣列，表示虛擬機器畫面的縮圖影像。 |IVMDisplay 縮圖屬性 (VPCCOMInterfaces .h) '
ms.assetid: e7b57f16-eec1-4461-acfb-742976eff14a
keywords:
- 縮圖屬性虛擬電腦
- 縮圖屬性 Virtual PC，IVMDisplay 介面
- IVMDisplay 介面 Virtual PC，縮圖屬性
topic_type:
- apiref
api_name:
- IVMDisplay.Thumbnail
- IVMDisplay.get_Thumbnail
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7a558a551972bb76558dcd60223d8ddc29783aeaa23e6dbe9263f34642c1c3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119473328"
---
# <a name="ivmdisplaythumbnail-property"></a>IVMDisplay：：縮圖屬性

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取圖元的陣列，表示虛擬機器畫面的縮圖影像。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_Thumbnail(
  [out, retval] VARIANT *thumbnailImage
);
```



## <a name="property-value"></a>屬性值

型別 VT \_ ARRAY \| VT variant 的變數 \_ ，其中包含 vt UI4 型別的專案 \_ ，縮圖中的每個圖元都有一個。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                    | 意義                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                       | 作業成功。<br/>     |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>         | 參數為 **Null**。<br/>        |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl> | 已發生未預期的錯誤。<br/> |



## <a name="remarks"></a>備註

這個介面會傳回比 [**\_ GenerateThumbnail**](ivmdisplay--generatethumbnail.md)方法更有效率的縮圖，但可從腳本用戶端使用。 縮圖一律為64圖元寬乘以48圖元高。 每個圖元都是32位。 陣列中的第一個64元素是縮圖中的第一個資料列，下一個64元素是第二個數據列，依此類推。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDisplay 定義為960895e9-f743-4498-96aa-261f867e7fc5<br/>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMDisplay**](ivmdisplay.md)
</dt> </dl>

 

