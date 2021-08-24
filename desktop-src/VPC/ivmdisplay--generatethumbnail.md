---
title: 'IVMDisplay _GenerateThumbnail 方法 (VPCCOMInterfaces .h) '
description: '抓取圖元的陣列，表示虛擬機器畫面的縮圖影像。 |IVMDisplay _GenerateThumbnail 方法 (VPCCOMInterfaces .h) '
ms.assetid: c97bb0ff-55cd-491f-a706-0ba15c9a6b54
keywords:
- _GenerateThumbnail 方法 Virtual PC
- _GenerateThumbnail 方法 Virtual PC，IVMDisplay 介面
- IVMDisplay 介面 Virtual PC，_GenerateThumbnail 方法
topic_type:
- apiref
api_name:
- IVMDisplay._GenerateThumbnail
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5decd1b3c55ab6513408a81eb37d422fac495334fb545c4cad4806050a8af7b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654368"
---
# <a name="ivmdisplay_generatethumbnail-method"></a>IVMDisplay：： \_ GenerateThumbnail 方法

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取圖元的陣列，表示虛擬機器畫面的縮圖影像。

## <a name="syntax"></a>語法


```C++
HRESULT _GenerateThumbnail(
  [out] unsigned long thumbnailImage[3072]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*thumbnailImage* \[擴展\]
</dt> <dd>

圖元的陣列，表示虛擬機器畫面的縮圖影像。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                 | 描述                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                       | 作業成功。<br/>     |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>         | 參數為 **Null**。<br/>        |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl> | 已發生未預期的錯誤。<br/> |



 

## <a name="remarks"></a>備註

此介面會比 [**縮圖**](ivmdisplay-thumbnail.md) 屬性更有效率地傳回縮圖，但無法從腳本用戶端使用。 縮圖一律為64圖元寬乘以48圖元高。 每個圖元都是32位，其中的前8個位代表圖元的藍色值，下8個位代表圖元的綠色值，而下一個8位代表圖元的紅色值。 陣列中的第一個64元素是縮圖的第一個資料列，下一個64元素是第二個數據列，依此類推。 這個方法會傳回靜態的圖元陣列，這比傳回 **VARIANT** 值的 **SAFEARRAY** 更有效率，但與腳本用戶端不相容。

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

 

