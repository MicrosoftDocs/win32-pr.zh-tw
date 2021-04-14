---
description: 使用自訂資料格式處理常式來擴充剪貼簿。
title: 如何建立資料處理程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ecc08769068d975c1fa16ef1385f362c67e43c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991566"
---
# <a name="how-to-create-data-handlers"></a>如何建立資料處理程式

將檔案複製到剪貼簿或拖放時，Shell 會建立支援各種標準 [剪貼簿格式](dragdrop.md)的資料物件。 針對特定檔案類型的檔案，您可以藉由執行和註冊 *資料處理程式* 來擴充可用的剪貼簿格式。 當傳送檔案類型的檔案時，如果使用其中一種自訂格式，Shell 會將對資料物件之 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) 介面的呼叫委派給資料處理程式。

[建立 shell](handlers.md)擴充處理常式時，會討論如何執行和註冊 shell 擴充處理常式的一般程式。 本檔著重于資料處理程式專屬的實作為這些層面。

-   [執行資料處理程式](#step-1-implementing-data-handlers)
-   [註冊資料處理程式](#step-2-registering-data-handlers)
-   [相關主題](#related-topics)

## <a name="instructions"></a>指示

### <a name="step-1-implementing-data-handlers"></a>步驟1：執行資料處理程式

如同所有 Shell 延伸模組處理常式，資料處理程式都是同進程元件物件模型， (COM) 物件實作為 Dll。 除了 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)： [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) 和 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)外，還會匯出兩個介面。

Shell 會透過其 [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) 介面初始化處理常式。 它會使用此介面來要求 (CLSID) 的處理常式類別識別碼，並提供該檔案的名稱。 如需如何執行 Shell 延伸模組處理常式（包括 **IPersistFile** 介面）的一般討論，請參閱 [建立 shell 擴充處理](handlers.md)程式。

當資料處理程式初始化之後，如果使用其中一種自訂格式，Shell 會將來自資料物件的呼叫委派給處理常式的 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) 介面。

### <a name="step-2-registering-data-handlers"></a>步驟2：註冊資料處理程式

資料處理程式會在檔案類型的 *ProgID* 子機碼下註冊，如下所示： **HKEY \_ 類別 \_ 根目錄** \\ *ProgID* \\ **shellex** \\ **DataHandler**

針對 **DataHandler** 下的處理常式建立名為的子機碼，並將該處理常式子機碼的預設值設定為處理常式 CLSID GUID 的字串形式。 如需如何註冊 Shell 擴充處理常式的一般討論，請參閱 [建立 Shell 擴充處理](handlers.md)程式。

下列範例說明可針對 myp 檔案類型啟用資料處理程式的登錄專案。

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
      Shellex
         DataHandler
            (Default) = {00000000-1111-2222-3333-444444444444}
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立 Shell 擴充功能處理常式](handlers.md)
</dt> <dt>

[**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> <dt>

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)
</dt> </dl>

 

 
