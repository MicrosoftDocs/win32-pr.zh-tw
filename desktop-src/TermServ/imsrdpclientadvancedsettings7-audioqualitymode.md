---
title: IMsRdpClientAdvancedSettings7 AudioQualityMode 屬性
description: 指定或抓取值，指出重新導向音訊的音訊品質模式設定。 根據預設，這會設定為0。
ms.assetid: 9945c524-ca50-41ae-a7cf-1386cd758c0f
ms.tgt_platform: multiple
keywords:
- AudioQualityMode 屬性遠端桌面服務
- AudioQualityMode 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，AudioQualityMode 屬性
- AudioQualityMode 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，AudioQualityMode 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.AudioQualityMode
- IMsRdpClientAdvancedSettings7.get_AudioQualityMode
- IMsRdpClientAdvancedSettings7.put_AudioQualityMode
- IMsRdpClientAdvancedSettings8.AudioQualityMode
- IMsRdpClientAdvancedSettings8.get_AudioQualityMode
- IMsRdpClientAdvancedSettings8.put_AudioQualityMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1635c2ed01144a640b624a014959a4847ae5f746502267444d958a20b959eef9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001306"
---
# <a name="imsrdpclientadvancedsettings7audioqualitymode-property"></a>IMsRdpClientAdvancedSettings7：： AudioQualityMode 屬性

指定或抓取值，指出重新導向音訊的音訊品質模式設定。 根據預設，這會設定為0。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_AudioQualityMode(
  [in]          UINT audioQualityMode
);

HRESULT get_AudioQualityMode(
  [out, retval] UINT *pAudioQualityMode
);
```



## <a name="property-value"></a>屬性值

指定音訊品質模式的值。

可能的值包括：

<dt>

0
</dt> <dd>

動態音訊品質。 這是預設的音訊品質設定。 伺服器會動態調整音訊輸出品質，以回應網路狀況和用戶端和伺服器功能。

</dd> <dt>

1
</dt> <dd>

中度音訊品質。 伺服器會針對音訊輸出使用固定但壓縮的格式。

</dd> <dt>

2
</dt> <dd>

高音訊品質。 伺服器以未壓縮 PCM 格式提供音訊輸出，延遲的處理負荷較低。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7<br/>                                                                             |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                                |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 定義為26036036-4010-4578-8091-0db9a1edf9c3<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





