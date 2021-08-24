---
title: 'IEnumBackgroundCopyFiles 介面 (>deliveryoptimization .h) '
description: 您可以使用 IEnumBackgroundCopyFiles 介面來列舉作業所包含的檔案。 若要取得 IEnumBackgroundCopyFiles 介面指標，請呼叫 IBackgroundCopyJob EnumFiles 方法。
ms.assetid: 539973BA-2756-4163-9D8B-4B7C0A708A8D
keywords:
- IEnumBackgroundCopyFiles 介面
- IEnumBackgroundCopyFiles 介面，說明
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c6cf97975d583a99145e32482bc097ebd6ce3cc052e62560a34f7f78c1f88ae6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635678"
---
# <a name="ienumbackgroundcopyfiles-interface"></a>IEnumBackgroundCopyFiles 介面

您可以使用 **IEnumBackgroundCopyFiles** 介面來列舉作業所包含的檔案。 若要取得 **IEnumBackgroundCopyFiles** 介面指標，請呼叫 [**IBackgroundCopyJob：： EnumFiles**](ibackgroundcopyjob-enumfiles.md) 方法。

## <a name="members"></a>成員

**IEnumBackgroundCopyFiles** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IEnumBackgroundCopyFiles** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IEnumBackgroundCopyFiles** 介面具有這些方法。



| 方法                                                | 描述                                                                   |
|:------------------------------------------------------|:------------------------------------------------------------------------------|
| [**GetCount**](ienumbackgroundcopyfiles-getcount.md) | 捕獲列舉中的專案數。<br/>                  |
| [**下一步**](ienumbackgroundcopyfiles-next.md)         | 擷取列舉型別序列中指定的項目數目。<br/> |
| [**重設**](ienumbackgroundcopyfiles-reset.md)       | 將列舉序列重設為開頭。<br/>                  |
| [**跳過**](ienumbackgroundcopyfiles-skip.md)         | 略過列舉序列中指定的項目數目。<br/>     |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | WindowsServer， \[ 僅限1709版桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>Deliveryoptimization。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IEnumBackgroundCopyFiles 定義為 CA51E165-C365-424C-8D41-24AAA4FF3C40<br/>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBackgroundCopyJob：： EnumFiles**](ibackgroundcopyjob-enumfiles.md)
</dt> </dl>

 

