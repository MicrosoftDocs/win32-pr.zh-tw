---
description: IMediaLocator 介面會提供方法，在 (DES) 的 DirectShow 編輯服務中驗證檔案名。
ms.assetid: 6c1ae957-a2be-454b-9451-772e4a670677
title: 'IMediaLocator 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9664bf793e989c5975bcef0e712a550399c4ddee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998378"
---
# <a name="imedialocator-interface"></a>IMediaLocator 介面

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`IMediaLocator`介面會提供方法，在 (DES) 的[DirectShow 編輯服務](directshow-editing-services.md)中驗證檔案名。 使用這個介面可確保指定的檔案名和路徑對應至現有的檔案。 這個介面也提供一種方式來搜尋其他位置的檔案，以及顯示 **開啟** 的對話方塊，讓使用者可以找到檔案。

媒體定位器會執行這個介面。 時間軸和轉譯引擎也支援透過下列方法進行的檔案名驗證：

-   [**IAMTimeline：： ValidateSourceNames**](iamtimeline-validatesourcenames.md)：在時間軸中驗證和更新檔案名。
-   [**IRenderEngine：： SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md)：指定轉譯引擎如何在轉譯時驗證檔案名。

DES 應用程式通常會呼叫這些方法，而不是直接建立媒體定位器的實例。 如需詳細資訊，請參閱 [使用媒體定位器](using-the-media-locator.md)。

## <a name="members"></a>成員

**IMediaLocator** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IMediaLocator** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IMediaLocator** 介面具有這些方法。



| 方法                                                     | 描述                                                                        |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**AddFoundLocation**](imedialocator-addfoundlocation.md) | 將目錄新增至目錄快取。<br/>                                |
| [**FindMediaFile**](imedialocator-findmediafile.md)       | 搜尋檔案，如果成功，則會抓取檔案的路徑。<br/> |



 

## <a name="remarks"></a>備註

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



 

 
