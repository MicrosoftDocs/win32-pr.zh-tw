---
description: IDxtKey 介面會設定金鑰轉換的屬性。此介面是在內部由 DirectShow 編輯服務 (DES) 轉譯金鑰轉換時使用。
ms.assetid: b929bf0c-8aaf-456e-b692-e23d88e480dd
title: 'IDxtKey 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d967d15dededf879ffd08671aac00e7892aa8ad2f2c1a39ce478f7f9f3e4db90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792358"
---
# <a name="idxtkey-interface"></a>IDxtKey 介面

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`IDxtKey`介面會設定[金鑰](key-transition.md)轉換的屬性。

此介面是在內部由 DirectShow 編輯服務 (DES) 轉譯金鑰轉換時使用。 DES 應用程式不需要使用此介面。 若要在 DES 的轉換上設定屬性，請使用 [**IPropertySetter**](ipropertysetter.md) 介面。

## <a name="members"></a>成員

**IDxtKey** 介面繼承自 **IDXEffect**。 **IDxtKey** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IDxtKey** 介面具有這些方法。



| 方法                                            | 描述                                                                            |
|:--------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**取得 \_ 色調**](idxtkey-get-hue.md)               | 抓取要做為索引鍵的色調值。<br/>                                    |
| [**取得 \_ 反轉**](idxtkey-get-invert.md)         | 抓取布林值，指出金鑰作業是否反轉。<br/> |
| [**取得 \_ KeyType**](idxtkey-get-keytype.md)       | 捕獲索引鍵的類型。<br/>                                                  |
| [**取得 \_ 亮度**](idxtkey-get-luminance.md)   | 抓取要作為索引鍵的亮度值。<br/>                              |
| [**取得 \_ RGB**](idxtkey-get-rgb.md)               | 抓取要作為索引鍵的 RGB 色彩。<br/>                                    |
| [**取得 \_ 相似性**](idxtkey-get-similarity.md) | 抓取變成透明的色彩資料範圍。<br/>                 |
| [**put \_ 色調**](idxtkey-put-hue.md)               | 指定要做為索引鍵的色調值。<br/>                                    |
| [**put \_ 反轉**](idxtkey-put-invert.md)         | 指定索引鍵作業是否反轉。<br/>                            |
| [**put \_ KeyType**](idxtkey-put-keytype.md)       | 指定索引鍵的類型。<br/>                                                  |
| [**put \_ 亮度**](idxtkey-put-luminance.md)   | 指定要做為索引鍵的亮度值。<br/>                              |
| [**put \_ RGB**](idxtkey-put-rgb.md)               | 指定要做為索引鍵的 RGB 色彩。<br/>                                    |
| [**放置 \_ 相似性**](idxtkey-put-similarity.md) | 指定變成透明的色彩資料範圍。<br/>                 |



 

## <a name="remarks"></a>備註

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載[Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



 

 




