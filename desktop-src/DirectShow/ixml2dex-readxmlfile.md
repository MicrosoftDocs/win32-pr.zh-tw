---
description: ReadXMLFile 方法會載入 XML 專案檔。
ms.assetid: 8269da74-fb33-42cf-ae8c-fe3d7db27aea
title: 'IXml2Dex：： ReadXMLFile 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.ReadXMLFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 37df0c93a17dadc2f6d6fbf94a662b89bf9630a0b0861f5bf5a0c676f7d369fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952437"
---
# <a name="ixml2dexreadxmlfile-method"></a>IXml2Dex：： ReadXMLFile 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`ReadXMLFile`方法會載入 XML 專案檔。 這個方法會建立 XML 檔案中表示的所有物件的實例，並將其插入至時間軸，以及套用任何針對時間軸提供的屬性，例如畫面播放速率或預設效果。

## <a name="syntax"></a>語法


```C++
HRESULT ReadXMLFile(
   IUnknown *pTimeline,
   BSTR     XMLName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pTimeline* 
</dt> <dd>

時間軸物件的 **IUnknown** 介面指標。

</dd> <dt>

*XMLName* 
</dt> <dd>

字串，指定要載入的檔案名。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 HRESULT 值。 可能的值如下。



| 傳回碼                                                                                                  | 描述                    |
|--------------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                         | Success<br/>             |
| <dl> <dt>**VFW \_ E \_ 不正確 \_ 檔 \_ 格式**</dt> </dl> | 不正確檔案格式<br/> |



 

## <a name="remarks"></a>備註

這個方法不會在插入 XML 檔案中定義的新物件之前，從時間軸清除現有的物件。 如果您需要重新整理現有的時間軸，請先呼叫 [**IAMTimeline：： ClearAllGroups**](iamtimeline-clearallgroups.md) 。

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載[Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | Internet Explorer 4.0 或更新版本<br/>                                               |
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IXml2Dex 介面**](ixml2dex.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




