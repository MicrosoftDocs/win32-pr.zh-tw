---
description: ITablet3 介面啟用多點觸控查詢以進行輸入。
ms.assetid: 949f2d83-7761-4d60-b8fe-5a9ac7567238
title: ITablet3 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: b774ab5626d1eab5d8f4179b27924686fed56661fb776039a65ff40b3b64ebba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449841"
---
# <a name="itablet3-interface"></a>ITablet3 介面

ITablet3 介面啟用多點觸控查詢以進行輸入。

## <a name="members"></a>成員

**ITablet3** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **ITablet3** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ITablet3** 介面具有這些方法。



| 方法                                                  | 描述                                                         |
|:--------------------------------------------------------|:--------------------------------------------------------------------|
| [**GetMaximumCursors**](itablet3-getmaximumcursors.md) | 抓取支援的輸入數目上限。<br/>        |
| [**isMultiTouch**](itablet3-ismultitouch.md)           | 指出是否已啟用此物件的多點觸控功能。<br/> |



 

## <a name="remarks"></a>備註

開發人員不應使用此介面

下列程式碼說明如何定義 **ITablet3** 介面。

``` syntax
[
  object,
  uuid(AC0E3951-0A2F-448E-88D0-49DA0C453460)
  pointer_default(unique)
]
interface ITablet3 : IUnknown
{
    HRESULT IsMultiTouch([out] BOOL *pIsMultiTouch);

    HRESULT GetMaximumCursors([out] ULONG *pMaximumCursors);
};
  
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                |
| 程式庫<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

