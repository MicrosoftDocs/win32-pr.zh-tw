---
description: 如何執行和註冊 drop handler。
title: 如何建立 Drop 處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081b4349ba36a12670458a453b0622475d59d755
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192688"
---
# <a name="how-to-create-drop-handlers"></a>如何建立 Drop 處理常式

依預設，檔案不會放置目標。 您可以藉由執行和註冊卸載 *處理常式*，讓 [檔案類型](fa-file-types.md)的成員成為卸載目標。

如果已針對檔案類型註冊卸載處理常式，每當在檔案類型的成員上拖曳物件時，就會呼叫該處理常式。 Shell 會藉由在處理常式的 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 介面上呼叫適當的方法來管理作業。

[建立 shell](handlers.md)擴充處理常式時，會討論如何執行和註冊 shell 擴充處理常式的一般程式。 本檔著重于卸載處理常式特定的執行層面。

## <a name="instructions"></a>指示

### <a name="step-1-implementing-drop-handlers"></a>步驟1：執行 Drop 處理常式

就像所有 Shell 擴充處理常式一樣，卸載處理常式也是實作為 Dll (COM) 物件的同進程元件物件模型。 除了 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)： [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) 和 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget)外，還會匯出兩個介面。

Shell 會透過其 [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) 介面初始化處理常式。 它會使用此介面來要求 (CLSID) 的處理常式類別識別碼，並提供該檔案的名稱。 如需如何執行 Shell 延伸模組處理常式（包括 **IPersistFile** 介面）的一般討論，請參閱 [建立 shell 擴充處理](handlers.md)程式。

當卸載處理常式初始化後，Shell 會在處理常式的 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 介面上呼叫適當的方法。

### <a name="step-2-registering-drop-handlers"></a>步驟2：註冊 Drop 處理常式

捨棄處理常式會在此檔案類型的子機碼下註冊。

```
HKEY_CLASSES_ROOT
   ProgID
      shellex
         DropHandler
```

針對處理常式建立名為 **DropHandler** 的子機碼，並將子機碼的預設值設定為處理常式 CLSID GUID 的字串形式。 如需如何註冊 Shell 擴充處理常式的一般討論，請參閱 [建立 Shell 擴充處理](handlers.md)程式。

下列範例說明可針對 myp 檔案類型啟用 drop handler 的登錄專案。

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         DropHandler
            (Default) = {00000000-1111-2222-3333-444444444444}
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立 Shell 擴充功能處理常式](handlers.md)
</dt> <dt>

[**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget)
</dt> <dt>

[**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> </dl>

 

 
