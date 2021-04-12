---
title: ShowMessageAction 物件
description: 針對腳本，表示在工作啟動時顯示訊息方塊的動作。
ms.assetid: fdd22eef-965c-4a81-954c-66011c435ab9
keywords:
- ShowMessageAction 物件工作排程器
- ShowMessageAction 物件工作排程器，說明
topic_type:
- apiref
api_name:
- ShowMessageAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef1e500f0492ad010e88719a467fda38f85e184c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384230"
---
# <a name="showmessageaction-object"></a>ShowMessageAction 物件

\[不再支援此物件。 您可以使用 IExecAction 搭配 Windows 腳本 [**MsgBox 函數**](/previous-versions/sfw6660x(v=vs.80)) ，在使用者會話中顯示訊息。\]

針對腳本，表示在工作啟動時顯示訊息方塊的動作。

## <a name="members"></a>成員

**ShowMessageAction** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**ShowMessageAction** 物件具有這些屬性。



| 屬性                                                        | 存取類型           | Description                                                                                               |
|:----------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**Id**](action-id.md)<br/>                              | 讀取/寫入<br/> | 繼承自 [**動作**](action.md) 物件。 取得或設定動作的識別碼。<br/> |
| [**MessageBody**](showmessageaction-messagebody.md)<br/> | 讀取/寫入<br/> | 取得或設定訊息方塊中顯示的郵件內文。<br/>                |
| [**標題**](showmessageaction-title.md)<br/>             | 讀取/寫入<br/> | 取得或設定訊息方塊的標題。<br/>                                                     |
| [**類型**](action-type.md)<br/>                          | 唯讀<br/>  | 繼承自 [**動作**](action.md) 物件。 取得動作的類型。<br/>               |



 

## <a name="remarks"></a>備註

對於包含訊息方塊動作的工作，如果工作已啟動且工作具有互動式登入類型，就會顯示訊息方塊。 若要將工作登入類型設定為 interactive，請在工作主體的 [**LogonType**](principal-logontype.md)屬性中，或在 [**TaskFolder. RegisterTask**](taskfolder-registertask.md)或 [**TaskFolder**](taskfolder-registertaskdefinition.md)的 *LogonType* 參數中指定 3 (工作登入 **\_ \_ 互動式 \_ 權杖**) 或 4 (工作 **登入 \_ \_ 群組**) 。

針對工作讀取或撰寫您自己的 XML 時，會使用工作排程器架構的 [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) 元素來指定訊息方塊動作。

## <a name="examples"></a>範例

如需此腳本物件的詳細資訊和範例程式碼，請參閱 [ (腳本) 的訊息方塊範例 ](/previous-versions//aa381916(v=vs.85))。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                    |
| 伺服器支援結束<br/>    | Windows Server 2008 R2<br/>                                                       |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

