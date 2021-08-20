---
description: 使用 Shell 擴充功能來執行複製勾點處理常式。
ms.assetid: 05808281-84fb-402d-9fa1-3a747b29d030
title: 如何建立複製勾點處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19a20831103d26233f76f64f32d07bf50977a746669fff7e5562da159e14027d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117679087"
---
# <a name="how-to-create-copy-hook-handlers"></a>如何建立複製勾點處理常式

[建立 shell](handlers.md)擴充處理常式時，會討論如何執行和註冊 shell 擴充處理常式的一般程式。 本檔著重于複製攔截處理常式特定的執行層面。

-   [執行複製勾點處理常式](#step-1-implementing-copy-hook-handlers)
-   [註冊複製勾點處理常式](#step-2-registering-copy-hook-handlers)
-   [相關主題](#related-topics)

## <a name="instructions"></a>指示

### <a name="step-1-implementing-copy-hook-handlers"></a>步驟1：執行複製勾點處理常式

如同所有 Shell 延伸模組處理常式，複製攔截處理常式也是實作為 Dll (COM) 物件的同進程元件物件模型。 除了 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)： [**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85))之外，也會匯出一個介面。 Shell 會直接初始化處理常式，因此不需要初始化介面（例如 [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)）。

[**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85))介面具有單一方法 [**ICopyHook：： CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85))。 當即將移動資料夾時，Shell 會呼叫這個方法。 它會傳入各種資訊，包括：

-   資料夾的名稱。
-   資料夾的目的地或新名稱。
-   正在嘗試的作業。
-   來源和目的資料夾的屬性。
-   可以用來顯示使用者介面的視窗控制碼。

呼叫處理常式的 [**ICopyHook：： CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)) 方法時，它會傳回下列三個值的其中一個，以指示 Shell 應如何繼續進行。



| 值    | 描述                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| IDYES    | 允許操作。                                                                                                                            |
| IDNO     | 防止此資料夾上的操作。 Shell 可以繼續執行任何其他已核准的作業，例如批次複製作業。 |
| IDCANCEL | 防止目前的作業，並取消任何暫止的作業。                                                                               |



 

### <a name="step-2-registering-copy-hook-handlers"></a>步驟2：註冊複製勾點處理常式

資料夾的複製勾點處理常式會在 **HKEY \_ 類別的 \_ 根目錄** \\  \\ **shellex** \\ **CopyHookHandlers** 子機碼下註冊。 針對處理常式建立名為 **CopyHookHandlers** 的子機碼，並將子機碼的預設值設定為處理常式之類別識別碼的字串格式， (CLSID) GUID。

下列範例會將 **MyCopyHandler** 子機碼新增至 Shell 的複製攔截處理常式清單。

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         CopyHookHandlers
            MyCopyHandler
               (Default) = {MyCopyHandler CLSID GUID}
```

印表機物件的複製勾點處理常式基本上是以相同方式註冊。 唯一的差別在於您必須在 **HKEY \_ 類別的 \_ 根** 印表機子機碼下註冊它們 \\  。

## <a name="remarks"></a>備註

一般情況下，使用者和應用程式可以複製、移動、刪除或重新命名資料夾，但有一些限制。 藉由執行複製勾點處理常式，您可以控制是否進行這些作業。 例如，執行這類處理常式可讓您防止重要的資料夾重新命名或刪除。 也可以針對印表機物件來執行複製勾點處理常式。

複製勾點處理常式是全域的。 Shell 會在每次應用程式或使用者嘗試複製、移動、刪除或重新命名資料夾或印表機物件時，呼叫所有已註冊的處理常式。 處理常式不會執行作業本身。 只核准或 vetoes。 如果所有處理常式都已核准，則 Shell 會執行作業。 如果有任何處理程式 vetoes 作業，就會取消它，而不會呼叫剩餘的處理常式。 複製攔截處理常式不會收到作業成功或失敗的通知，因此不能用來監視檔案作業。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立 Shell 擴充功能處理常式](handlers.md)
</dt> <dt>

[**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85))
</dt> </dl>

 

 
