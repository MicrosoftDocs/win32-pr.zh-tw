---
title: ClientSpec 列舉
description: 搭配 ClientProtocolSpec 屬性使用，以指定用戶端與伺服器之間使用的遠端桌面通訊協定。
ms.assetid: BFB2CD3C-04BF-4CB3-B156-8B08AE697327
ms.tgt_platform: multiple
keywords:
- ClientSpec 列舉遠端桌面服務
topic_type:
- apiref
api_name:
- ClientSpec
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f52fbdbaa37c392de727dd2640580800d813d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966910"
---
# <a name="clientspec-enumeration"></a>ClientSpec 列舉

搭配 [**ClientProtocolSpec**](imsrdpclientadvancedsettings8-clientprotocolspec.md) 屬性使用，以指定用戶端與伺服器之間使用的遠端桌面通訊協定。

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  FullMode        = 0,
  ThinClientMode,
  SmallCacheMode
} ClientSpec;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="FullMode"></span><span id="fullmode"></span><span id="FULLMODE"></span>**FullMode**
</dt> <dd>

通訊協定已完整 Windows 8 遠端桌面通訊協定。

</dd> <dt>

<span id="ThinClientMode"></span><span id="thinclientmode"></span><span id="THINCLIENTMODE"></span>**ThinClientMode**
</dt> <dd>

此通訊協定僅限於使用 Windows 7 SP1 RemoteFX 編解碼器和較小的快取。 所有其他編解碼器皆已停用。 此通訊協定具有最小的記憶體使用量。

</dd> <dt>

<span id="SmallCacheMode"></span><span id="smallcachemode"></span><span id="SMALLCACHEMODE"></span>**SmallCacheMode**
</dt> <dd>

通訊協定與 **FullMode** 相同，但它使用較小的快取。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientAdvancedSettings8::ClientProtocolSpec**](imsrdpclientadvancedsettings8-clientprotocolspec.md)
</dt> </dl>

 

 





