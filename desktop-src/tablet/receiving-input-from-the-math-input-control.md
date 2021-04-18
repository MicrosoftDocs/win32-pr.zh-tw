---
description: 本節說明如何使用 Active Template Library (ATL) 和元件物件模型 (COM) ，從數學輸入控制項取出 MathML 標記。
ms.assetid: 352d2a0c-8275-4fe4-b523-4c74126ffadf
title: 從數學輸入控制項接收輸入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 830c8f57bb7b27c305928cf68b658dcc37ede5d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971598"
---
# <a name="receiving-input-from-the-math-input-control"></a>從數學輸入控制項接收輸入

本節說明如何使用 Active Template Library (ATL) 和元件物件模型 (COM) ，從數學輸入控制項取出 MathML 標記。

若要從數學輸入控制項取出辨識的數學方程式，您可以覆寫按下 [插入] 按鈕時所發生的行為。 若要這樣做，您必須設定一個事件處理常式，以執行 [**\_ IMathInputControlEvents**](/windows/win32/api/micaut/nn-micaut-_imathinputcontrolevents)介面所支援的各種事件。 設定事件處理常式牽涉到針對您想要支援的事件執行下列步驟， (在此案例中插入) 。

-   [建立包含事件接收器的範本類別](#create-a-template-class-that-contains-event-sinks)
-   [設定事件處理常式](#set-up-the-event-handlers)
-   [在您的主要類別中繼承事件處理常式類別](#inherit-the-event-handler-class-in-your-main-class)
-   [初始化您的類別，以繼承事件接收 (s) ](#initialize-your-class-to-inherit-the-event-sinks)

## <a name="create-a-template-class-that-contains-event-sinks"></a>建立包含事件接收器的範本類別

當您在執行使用數學輸入控制項的事件接收時，您必須先指定接收識別碼。然後，您必須建立繼承自事件、事件控制處理常式和數學輸入控制項事件介面的樣板類別。 下列程式碼示範如何設定接收識別碼，並建立繼承自必要介面的這類範本類別 CMathInputControlEventHandler。 此範本類別也會設定為具有私用未知介面指標，此指標將用來在初始化時將數學輸入控制項傳遞給它，並使用 m \_ ulAdviseCount 成員來計算建議/unadvise 的呼叫次數。


```
  
#pragma once
static const int MATHINPUTCONTROL_SINK_ID = 1 ;

template <class T>
class ATL_NO_VTABLE CMathInputControlEventHandler :
    public IDispEventSimpleImpl<MATHINPUTCONTROL_SINK_ID, CMathInputControlEventHandler<T>, &__uuidof(_IMathInputControlEvents)>
{
private:
    IUnknown    *m_pUnknown;
    ULONG m_ulAdviseCount;
    CDialog *m_pMain;

```



> [!Note]  
> 如果您不是使用對話方塊，則在您的執行中，成員 **m \_ pMain** 應該不同。

 

現在您已有基本的範本類別，您必須為您將覆寫的事件處理常式提供向前宣告，然後必須為您將處理的事件設定接收對應。 下列程式碼示範如何設定 [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) 方法的事件處理常式，在使用者按一下數學輸入控制項上的 [插入] 按鈕時呼叫，然後按一下 [ [**關閉**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) ] 方法（當使用者按一下數學輸入控制項上的 [取消] 按鈕時呼叫）。


```
  
public:
    static const _ATL_FUNC_INFO OnMICInsertInfo; // = {CC_STDCALL, VT_I4, 1, {VT_BSTR}};
    static const _ATL_FUNC_INFO OnMICCloseInfo;  // = {CC_STDCALL, VT_I4, 0, {VT_EMPTY}};

    BEGIN_SINK_MAP(CMathInputControlEventHandler)
        SINK_ENTRY_INFO(MATHINPUTCONTROL_SINK_ID, __uuidof(_IMathInputControlEvents), DISPID_MICInsert, OnMICInsert, const_cast<_ATL_FUNC_INFO*>(&OnMICInsertInfo))
        SINK_ENTRY_INFO(MATHINPUTCONTROL_SINK_ID, __uuidof(_IMathInputControlEvents), DISPID_MICClose, OnMICClose, const_cast<_ATL_FUNC_INFO*>(&OnMICCloseInfo))  
    END_SINK_MAP()
```



由於您將使用數學輸入控制項，因此設定相關介面的內部參考將會很有用。 在範例類別中建立下列公用程式函式，以設定此參考。


```
    
  HRESULT Initialize(IUnknown *pUnknown, CDialog *pMain)
  {
    m_pMain  = pMain;
    m_pUnknown = pUnknown;
    m_ulAdviseCount = 0;
    return S_OK;
  }
  
```



## <a name="set-up-the-event-handlers"></a>設定事件處理常式

設定事件接收器之後，您將需要建立事件接收器的實作為。 在下列程式碼範例的兩個方法中，事件接收器會取出數學輸入控制項介面的控制碼。 在 [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) 函式中，辨識結果會顯示為 MathML，而且控制項會隱藏。 在 [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) 函式中，math input 控制項是隱藏的。


```
  
    // Methods
    HRESULT __stdcall OnMICInsert( BSTR bstrRecoResult)
    {
        CComQIPtr<IMathInputControl> spMIC(m_pUnknown);
        HRESULT hr=S_OK;
        if (spMIC)
        {           
            MessageBox(NULL,bstrRecoResult,L"Recognition Result",MB_OK);
            hr = spMIC->Hide();
            return hr;  
        }
        return E_FAIL;          
    }

    HRESULT __stdcall OnMICClose()
    {
        CComPtr<IMathInputControl> spMIC;
        HRESULT hr = m_pUnknown->QueryInterface<IMathInputControl>(&spMIC);
        if (SUCCEEDED(hr))
        {           
            hr = spMIC->Hide();
            return hr;  
        }
        return hr;                  
    }
};  
```



## <a name="inherit-the-event-handler-class-in-your-main-class"></a>在您的主要類別中繼承事件處理常式類別

在您完成範本類別之後，您必須將它繼承到您將在中設定數學輸入控制項的類別。 基於本指南的目的，這個類別是 CMIC TEST EVENTSDlg 的對話方塊 \_ \_ 。 在對話方塊標頭中，必須包含必要的標頭，而且您建立的範本類別必須被繼承。 您要在其中繼承的類別和事件處理常式必須具有向前宣告，才能實作為範本。 下列程式碼範例顯示如何完成這項操作。


```
#pragma once
#include <atlbase.h>
#include <atlwin.h>

// include for MIC
#include "micaut.h"

// include for event sinks
#include <iacom.h>
#include "mathinputcontroleventhandler.h"

class CMIC_TEST_EVENTSDlg;

const _ATL_FUNC_INFO CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::OnMICInsertInfo = {CC_STDCALL, VT_I4, 1, {VT_BSTR}};
const _ATL_FUNC_INFO CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::OnMICCloseInfo = {CC_STDCALL, VT_I4, 0, {VT_EMPTY}};

// CMIC_TEST_EVENTSDlg dialog
class CMIC_TEST_EVENTSDlg : public CDialog,
    public CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>
{
  public:
  CComPtr<IMathInputControl> m_spMIC; // Math Input Control

  
```



> [!Note]  
> 除非您已將類別命名為與範例相同，否則範本類型 **CMIC \_ TEST \_ EventsDlg** 將會不同。

 

## <a name="initialize-your-class-to-inherit-the-event-sinks"></a>初始化您的類別，以繼承事件接收 (s) 

當您將類別設定為繼承自範本類別之後，您就可以設定它來處理事件。 這會包含初始化類別以具有數學輸入控制項和呼叫類別的控制碼。 此外，用來處理事件的數學輸入控制項必須傳送至 CMathInputControlEventHandler 範例類別所繼承的 DispEventAdvise 方法。 下列程式碼會從範例類別中的 OnInitDialog 方法呼叫，以執行這些動作。


```
// includes for implementation
#include "micaut_i.c"

// include for event handler
#include "mathinputcontroleventhandler.h"

...

OnInitDialog{
  ...

  // TODO: Add extra initialization here
  CoInitialize(NULL);
  HRESULT hr = g_spMIC.CoCreateInstance(CLSID_MathInputControl);
  if (SUCCEEDED(hr)){
    hr = CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::Initialize(m_spMIC, this);
      if (SUCCEEDED(hr)){
        hr = CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::DispEventAdvise(m_spMIC);            
        if (SUCCEEDED(hr)){
          hr = m_spMIC->Show();  
        }
      }
    }
  }  
}
  
```



> [!Note]  
> \_在此範例中，範本類型 CMIC TEST \_ EventsDlg 將會不同，除非您已將類別命名為與範例相同。

 

 

 
