---
description: 傳回值，這個值表示平板電腦硬體的功能。
ms.assetid: 68936dab-3df4-42c4-9945-bcd525c996f3
title: ITablet：： GetHardwareCaps 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetHardwareCaps
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5ada3ad58699952bac5458ddd079abaf84f63bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851607"
---
# <a name="itabletgethardwarecaps-method"></a>ITablet：： GetHardwareCaps 方法

傳回值，這個值表示平板電腦硬體的功能。

## <a name="syntax"></a>語法


```C++
HRESULT GetHardwareCaps(
  [out] DWORD *pdwCaps
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pdwCaps* \[擴展\]
</dt> <dd>

代表平板電腦硬體功能的位旗標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>   | 成功。<br/>                       |
| <dl> <dt>**E \_ 失敗**</dt> </dl> | 發生未指定的錯誤。<br/> |



 

## <a name="remarks"></a>備註

*PdwCaps* 參數是一組用來描述平板電腦硬體功能的位旗標。 下表描述這些旗標。



| 旗標名稱                         | 值                 | 描述                                                                                                                    |
|-----------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------|
| THWC \_ 整合式<br/>       | 0x00000001<br/> | 指出顯示器和數位板會共用相同的表面。<br/>                                                    |
| THWC \_ CSR \_ 必須 \_ 接觸<br/> | 0x00000002<br/> | 表示資料指標必須在與裝置的實體連絡人之間，才能報告位置。<br/>                           |
| THWC \_ 硬 \_ 距離<br/>  | 0x00000004<br/> | 指出當游標進入並離開實體偵測範圍時，裝置可以產生事件。<br/> |
| THWC \_ PHYSID \_ CSR<br/>     | 0x00000008<br/> | 指出裝置可在硬體中唯一識別作用中的資料指標。<br/>                                      |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                              |
| 程式庫<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITablet 介面**](itablet.md)
</dt> </dl>

 

 




