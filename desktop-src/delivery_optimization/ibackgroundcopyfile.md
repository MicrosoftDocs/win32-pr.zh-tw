---
title: 'IBackgroundCopyFile 介面 (>deliveryoptimization .h) '
description: IBackgroundCopyFile 包含屬於作業一部分之檔案的相關資訊。 例如，您可以使用 IBackgroundCopyFile 方法來取出檔案的本機和遠端名稱，並傳送進度資訊。
ms.assetid: 463ED61A-D7C5-4B44-97CF-FDAA138CE9E3
keywords:
- IBackgroundCopyFile 介面
- IBackgroundCopyFile 介面，說明
topic_type:
- apiref
api_name:
- IBackgroundCopyFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e4a54a66dee87770326d2456cb384e9d77f15e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969581"
---
# <a name="ibackgroundcopyfile-interface"></a>IBackgroundCopyFile 介面

**IBackgroundCopyFile** 包含屬於作業一部分之檔案的相關資訊。 例如，您可以使用 **IBackgroundCopyFile** 方法來取出檔案的本機和遠端名稱，並傳送進度資訊。

若要取得 **IBackgroundCopyFile** 介面指標，請呼叫 [**IBackgroundCopyError：： GetFile**](ibackgroundcopyerror-getfile-method.md) 方法或 [**IEnumBackgroundCopyFiles：： Next**](ienumbackgroundcopyfiles-next.md) 方法。

## <a name="members"></a>成員

**IBackgroundCopyFile** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IBackgroundCopyFile** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IBackgroundCopyFile** 介面具有這些方法。



| 方法                                                            | 描述                                             |
|:------------------------------------------------------------------|:--------------------------------------------------------|
| [**GetLocalName**](ibackgroundcopyfile-getlocalname-method.md)   | 抓取檔案的本機名稱。<br/>        |
| [**GetProgress**](ibackgroundcopyfile-getprogress-method.md)     | 捕獲檔案傳輸的進度。<br/> |
| [**GetRemoteName**](ibackgroundcopyfile-getremotename-method.md) | 抓取檔案的遠端名稱。<br/>       |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>deliveryoptimization。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile 定義為01B7BD23-FB88-4A77-8490-5891D3E4653A<br/>              |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

