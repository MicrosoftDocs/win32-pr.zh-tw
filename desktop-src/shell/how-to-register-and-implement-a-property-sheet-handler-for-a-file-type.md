---
description: 當使用者以滑鼠右鍵按一下檔案類型的成員來顯示 [屬性] 屬性工作表時，Shell 會呼叫已註冊檔案類型的屬性工作表處理常式。 每個處理常式都可以在預設的屬性工作表中加入一個自訂頁面。
title: 如何註冊及執行檔案類型的屬性工作表處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77cf54886f7819fa910da23393c6db488ddfee72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991555"
---
# <a name="how-to-register-and-implement-a-property-sheet-handler-for-a-file-type"></a>如何註冊及執行檔案類型的屬性工作表處理常式

當使用者以滑鼠右鍵按一下檔案類型的成員來顯示 [屬性] 屬性工作表時，Shell 會呼叫已註冊檔案類型的屬性工作表處理常式。 每個處理常式都可以在預設的屬性工作表中加入一個自訂頁面。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   殼層

### <a name="prerequisites"></a>必要條件

-   對快速鍵功能表的瞭解

## <a name="instructions"></a>指示

### <a name="step-1-registering-a-property-sheet-handler-for-a-file-type"></a>步驟1：註冊檔案類型的屬性工作表處理常式

除了 (COM) 註冊的一般元件物件模型之外，還請將 **PropertySheetHandlers** 子機碼新增至與檔案類型相關聯之應用程式 ProgID 索引鍵的 **shellex** 子機碼中。 使用處理程式的名稱建立 **PropertySheetHandlers** 的子機碼，並將預設值設定為屬性工作表處理常式之類別識別碼的字串格式， (CLSID) GUID。

若要在屬性工作表中加入多個頁面，請為每個頁面註冊處理常式。 屬性工作表可以支援的最大頁面數目是32。 若要註冊多個處理常式，請在每個處理常式的 **shellex** 索引鍵下建立金鑰，並將預設值設定為處理常式的 CLSID GUID。 不需要為每個處理常式建立相異物件，這表示多個處理常式可以有相同的 GUID 值。 頁面將會依其索引鍵列在 [ **shellex**] 底下的順序顯示。

下列範例說明的登錄專案，可啟用 myp 檔案類型的兩個屬性工作表延伸模組處理常式。 在此範例中，會針對每個頁面使用個別的物件，但是單一物件也可用於兩者。

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {Page 1 Property Sheet Handler CLSID GUID}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet1.dll
            ThreadingModel = Apartment
      {Page 2 Property Sheet Handler CLSID GUID}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet2.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         PropertySheetHandlers
            MyPropSheet1
               (Default) = {Page1 Property Sheet Handler CLSID GUID}
            MyPropSheet2
               (Default) = {Page2 Property Sheet Handler CLSID GUID}
```

### <a name="step-2-implementing-a-property-sheet-handler-for-a-file-type"></a>步驟2：為檔案類型執行屬性工作表處理常式

除了 [屬性工作表處理常式如何運作](propsheet-handlers.md)的一般執行之外，檔案類型的屬性工作表處理常式也必須有適當的 [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) 介面執行。 只有 [**IShellPropSheetExt：： AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) 方法需要 nontoken 執行。 Shell 不會呼叫 [**IShellPropSheetExt：： ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage)。

[**IShellPropSheetExt：： AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages)方法可讓屬性工作表處理常式將頁面加入至屬性工作表。 方法有兩個輸入參數。 第一個 *lpfnAddPage* 是 [*AddPropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnaddpropsheetpage) 回呼函式的指標，它是用來為 Shell 提供將頁面加入至屬性工作表所需的資訊。 第二個 *lParam* 是 Shell 定義的值，不是由處理常式處理。 呼叫回呼函式時，它只會傳回給 Shell。

執行 [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) 的一般程式如下所示。

**執行 AddPages 方法**

1.  將適當的值指派給 [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) 結構的成員。 尤其是：
    -   將保存處理常式參考計數的變數指派給 **pcRefParent** 成員。 這種做法可防止在屬性工作表仍在顯示時卸載處理常式物件。
    -   您也可以執行 [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) 回呼函式，並將其指標指派給 **pfnCallback** 成員。 這個函式會在頁面建立時以及即將終結時呼叫。
2.  藉由將 [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) 結構傳遞至 [**CreatePropertySheetPage**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) 函式，建立頁面的 HPAGE 控制碼。
3.  呼叫 *lpfnAddPage* 所指向的函式。 將其第一個參數設定為上一個步驟中所建立的 HPAGE 控制碼。 將其第二個參數設定為由 Shell 傳遞給 [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages)的 *lParam* 值。
4.  任何與頁面相關聯的訊息都會傳遞至已指派給 [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3)結構之 **pfnDlgProc** 成員的對話方塊程式。
5.  如果您將 [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) 回呼函式指派給 **pfnCallback**，則會在頁面即將終結時呼叫它。 然後，您的處理常式可以執行任何所需的清除作業，例如釋出它所保留的任何參考。

下列程式碼範例說明簡單的 [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) 執行。


```C++
STDMETHODIMP CShellPropSheetExt::AddPages(LPFNADDPROPSHEETPAGE, lpfnAddPage, LPARAM lParam)
{
    PROPSHEETPAGE  psp;
    HPROPSHEETPAGE hPage;

    psp.dwSize        = sizeof(psp);
    psp.dwFlags       = PSP_USEREFPARENT | PSP_USETITLE | PSP_USECALLBACK;
    psp.hInstance     = g_hInst;
    psp.pszTemplate   = MAKEINTRESOURCE(IDD_PAGEDLG);
    psp.hIcon         = 0;
    psp.pszTitle      = TEXT("Extension Page");
    psp.pfnDlgProc    = (DLGPROC)PageDlgProc;
    psp.pcRefParent   = &g_DllRefCount;
    psp.pfnCallback   = PageCallbackProc;
    psp.lParam        = (LPARAM)this;

    hPage = CreatePropertySheetPage(&psp);
            
    if(hPage) 
    {
        if(lpfnAddPage(hPage, lParam))
        {
            this->AddRef();
            return S_OK;
        }
        else
        {
            DestroyPropertySheetPage(hPage);
        }
    }
    else
    {
        return E_OUTOFMEMORY;
    }
    return E_FAIL;
}
```



**G \_ hInst** 變數是 DLL 的實例控制碼，而 IDD \_ PAGEDLG 是頁面之對話方塊範本的資源識別碼。 **PageDlgProc** 函數是處理頁面訊息的對話方塊程式。 **G \_ DllRefCount** 變數會保存物件的參考計數。 [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages)方法會呼叫 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)來遞增計數。 不過，當頁面即將終結時， **PageCallbackProc** 回呼函數會釋放參考計數。

## <a name="remarks"></a>備註

如需如何註冊 Shell 擴充處理常式的一般討論，請參閱 [建立 Shell 擴充處理](handlers.md)程式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)
</dt> </dl>

 

 
