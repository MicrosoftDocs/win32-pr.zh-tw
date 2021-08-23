---
title: 'IBackgroundCopyFile5 介面 (>deliveryoptimization .h) '
description: 您可以使用這個介面來取得或設定傳遞最佳化 (執行) 檔案傳輸的一般屬性。
ms.assetid: 2D729717-62D2-4C69-92FE-F4289EC48DF1
keywords:
- IBackgroundCopyFile5 介面
- IBackgroundCopyFile5 介面，說明
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 369afa2f242faf1572b16f82aebc4ae18a8d501b5e3b806d74bb580beab3aa26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610358"
---
# <a name="ibackgroundcopyfile5-interface"></a>IBackgroundCopyFile5 介面

您可以使用這個介面來取得或設定傳遞最佳化 (執行) 檔案傳輸的一般屬性。

若要取得 **IBackgroundCopyFile5** 介面指標，請針對介面識別碼使用 __Uuidof (IBackgroundCopyFile5) 來呼叫 **IBackgroundCopyFile：： QueryInterface** 方法。

## <a name="members"></a>成員

**IBackgroundCopyFile5** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IBackgroundCopyFile5** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IBackgroundCopyFile5** 介面具有這些方法。



| 方法                                                  | 描述                                                         |
|:--------------------------------------------------------|:--------------------------------------------------------------------|
| [**GetProperty**](ibackgroundcopyfile5-getproperty.md) | 取得泛型 BackgroundCopyFile 屬性的值。<br/> |
| [**SetProperty**](ibackgroundcopyfile5-setproperty.md) | 設定泛型 BackgroundCopyFile 屬性的值。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | WindowsServer， \[ 僅限1709版桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>Deliveryoptimization。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile5 定義為85C1657F-DAFC-40E8-8834-DF18EA25717E<br/>             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> </dl>

 

