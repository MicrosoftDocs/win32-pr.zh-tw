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
# <a name="receiving-input-from-the-math-input-control"></a><span data-ttu-id="5d984-103">從數學輸入控制項接收輸入</span><span class="sxs-lookup"><span data-stu-id="5d984-103">Receiving Input from the Math Input Control</span></span>

<span data-ttu-id="5d984-104">本節說明如何使用 Active Template Library (ATL) 和元件物件模型 (COM) ，從數學輸入控制項取出 MathML 標記。</span><span class="sxs-lookup"><span data-stu-id="5d984-104">This section explains how to retrieve the MathML markup from the math input control using the Active Template Library (ATL) and the Component Object Model (COM).</span></span>

<span data-ttu-id="5d984-105">若要從數學輸入控制項取出辨識的數學方程式，您可以覆寫按下 [插入] 按鈕時所發生的行為。</span><span class="sxs-lookup"><span data-stu-id="5d984-105">To retrieve the recognized math equation from the math input control, you can override the behavior that happens when the insert button is pressed.</span></span> <span data-ttu-id="5d984-106">若要這樣做，您必須設定一個事件處理常式，以執行 [**\_ IMathInputControlEvents**](/windows/win32/api/micaut/nn-micaut-_imathinputcontrolevents)介面所支援的各種事件。</span><span class="sxs-lookup"><span data-stu-id="5d984-106">To do this, you will need to set up an event handler that implements the various events that are supported by the [**\_IMathInputControlEvents**](/windows/win32/api/micaut/nn-micaut-_imathinputcontrolevents) interface.</span></span> <span data-ttu-id="5d984-107">設定事件處理常式牽涉到針對您想要支援的事件執行下列步驟， (在此案例中插入) 。</span><span class="sxs-lookup"><span data-stu-id="5d984-107">Setting up the events handler involves the performing the following steps for the events you want to support (insert in this case).</span></span>

-   [<span data-ttu-id="5d984-108">建立包含事件接收器的範本類別</span><span class="sxs-lookup"><span data-stu-id="5d984-108">Create a template class that contains event sinks</span></span>](#create-a-template-class-that-contains-event-sinks)
-   [<span data-ttu-id="5d984-109">設定事件處理常式</span><span class="sxs-lookup"><span data-stu-id="5d984-109">Set up the event handlers</span></span>](#set-up-the-event-handlers)
-   [<span data-ttu-id="5d984-110">在您的主要類別中繼承事件處理常式類別</span><span class="sxs-lookup"><span data-stu-id="5d984-110">Inherit the event handler class in your main class</span></span>](#inherit-the-event-handler-class-in-your-main-class)
-   [<span data-ttu-id="5d984-111">初始化您的類別，以繼承事件接收 (s) </span><span class="sxs-lookup"><span data-stu-id="5d984-111">Initialize your class to inherit the event sink(s)</span></span>](#initialize-your-class-to-inherit-the-event-sinks)

## <a name="create-a-template-class-that-contains-event-sinks"></a><span data-ttu-id="5d984-112">建立包含事件接收器的範本類別</span><span class="sxs-lookup"><span data-stu-id="5d984-112">Create a template class that contains event sinks</span></span>

<span data-ttu-id="5d984-113">當您在執行使用數學輸入控制項的事件接收時，您必須先指定接收識別碼。然後，您必須建立繼承自事件、事件控制處理常式和數學輸入控制項事件介面的樣板類別。</span><span class="sxs-lookup"><span data-stu-id="5d984-113">When you are implementing an event sink that uses the math input control, you must first specify a sink id. You must then create a template class that inherits from the event, event control handler, and math input control event interfaces.</span></span> <span data-ttu-id="5d984-114">下列程式碼示範如何設定接收識別碼，並建立繼承自必要介面的這類範本類別 CMathInputControlEventHandler。</span><span class="sxs-lookup"><span data-stu-id="5d984-114">The following code shows how to set a sink id and create such a template class, CMathInputControlEventHandler, that inherits from the requisite interfaces.</span></span> <span data-ttu-id="5d984-115">此範本類別也會設定為具有私用未知介面指標，此指標將用來在初始化時將數學輸入控制項傳遞給它，並使用 m \_ ulAdviseCount 成員來計算建議/unadvise 的呼叫次數。</span><span class="sxs-lookup"><span data-stu-id="5d984-115">This template class also is set up to have a private unknown interface pointer that will be used to pass the math input control to it on initialization and the m\_ulAdviseCount member to count the number of calls to advise / unadvise.</span></span>


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
> <span data-ttu-id="5d984-116">如果您不是使用對話方塊，則在您的執行中，成員 **m \_ pMain** 應該不同。</span><span class="sxs-lookup"><span data-stu-id="5d984-116">The member **m\_pMain** should be different in your implementation if you are not using a dialog.</span></span>

 

<span data-ttu-id="5d984-117">現在您已有基本的範本類別，您必須為您將覆寫的事件處理常式提供向前宣告，然後必須為您將處理的事件設定接收對應。</span><span class="sxs-lookup"><span data-stu-id="5d984-117">Now that you have the basic template class, you must give a forward declaration for the event handlers that you will be overriding and must then set up a sink map for the events you will be handling.</span></span> <span data-ttu-id="5d984-118">下列程式碼示範如何設定 [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) 方法的事件處理常式，在使用者按一下數學輸入控制項上的 [插入] 按鈕時呼叫，然後按一下 [ [**關閉**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) ] 方法（當使用者按一下數學輸入控制項上的 [取消] 按鈕時呼叫）。</span><span class="sxs-lookup"><span data-stu-id="5d984-118">The following code shows how to set up event handlers for the [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) method, called when a user clicks the insert button on the math input control, and the [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) method, called when a user clicks the cancel button on the math input control.</span></span>


```
  
public:
    static const _ATL_FUNC_INFO OnMICInsertInfo; // = {CC_STDCALL, VT_I4, 1, {VT_BSTR}};
    static const _ATL_FUNC_INFO OnMICCloseInfo;  // = {CC_STDCALL, VT_I4, 0, {VT_EMPTY}};

    BEGIN_SINK_MAP(CMathInputControlEventHandler)
        SINK_ENTRY_INFO(MATHINPUTCONTROL_SINK_ID, __uuidof(_IMathInputControlEvents), DISPID_MICInsert, OnMICInsert, const_cast<_ATL_FUNC_INFO*>(&OnMICInsertInfo))
        SINK_ENTRY_INFO(MATHINPUTCONTROL_SINK_ID, __uuidof(_IMathInputControlEvents), DISPID_MICClose, OnMICClose, const_cast<_ATL_FUNC_INFO*>(&OnMICCloseInfo))  
    END_SINK_MAP()
```



<span data-ttu-id="5d984-119">由於您將使用數學輸入控制項，因此設定相關介面的內部參考將會很有用。</span><span class="sxs-lookup"><span data-stu-id="5d984-119">Since you will be working with the math input control, it will be useful to set an internal reference to the relevant interface.</span></span> <span data-ttu-id="5d984-120">在範例類別中建立下列公用程式函式，以設定此參考。</span><span class="sxs-lookup"><span data-stu-id="5d984-120">The following utility function is created in the example class to set this reference.</span></span>


```
    
  HRESULT Initialize(IUnknown *pUnknown, CDialog *pMain)
  {
    m_pMain  = pMain;
    m_pUnknown = pUnknown;
    m_ulAdviseCount = 0;
    return S_OK;
  }
  
```



## <a name="set-up-the-event-handlers"></a><span data-ttu-id="5d984-121">設定事件處理常式</span><span class="sxs-lookup"><span data-stu-id="5d984-121">Set up the event handlers</span></span>

<span data-ttu-id="5d984-122">設定事件接收器之後，您將需要建立事件接收器的實作為。</span><span class="sxs-lookup"><span data-stu-id="5d984-122">Once you have set up the event sinks, you will need to create your implementations of the event sinks.</span></span> <span data-ttu-id="5d984-123">在下列程式碼範例的兩個方法中，事件接收器會取出數學輸入控制項介面的控制碼。</span><span class="sxs-lookup"><span data-stu-id="5d984-123">In both of the methods in the following code example, the event sinks retrieve a handle to the math input control interface.</span></span> <span data-ttu-id="5d984-124">在 [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) 函式中，辨識結果會顯示為 MathML，而且控制項會隱藏。</span><span class="sxs-lookup"><span data-stu-id="5d984-124">In the [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) function, the recognition result is displayed as MathML and the control is hidden.</span></span> <span data-ttu-id="5d984-125">在 [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) 函式中，math input 控制項是隱藏的。</span><span class="sxs-lookup"><span data-stu-id="5d984-125">In the [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) function, the math input control is hidden.</span></span>


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



## <a name="inherit-the-event-handler-class-in-your-main-class"></a><span data-ttu-id="5d984-126">在您的主要類別中繼承事件處理常式類別</span><span class="sxs-lookup"><span data-stu-id="5d984-126">Inherit the event handler class in your main class</span></span>

<span data-ttu-id="5d984-127">在您完成範本類別之後，您必須將它繼承到您將在中設定數學輸入控制項的類別。</span><span class="sxs-lookup"><span data-stu-id="5d984-127">After you have your template class implemented, you will need to inherit it into the class that you will be setting up your math input control in.</span></span> <span data-ttu-id="5d984-128">基於本指南的目的，這個類別是 CMIC TEST EVENTSDlg 的對話方塊 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="5d984-128">For the purposes of this guide, this class is a dialog, CMIC\_TEST\_EVENTSDlg.</span></span> <span data-ttu-id="5d984-129">在對話方塊標頭中，必須包含必要的標頭，而且您建立的範本類別必須被繼承。</span><span class="sxs-lookup"><span data-stu-id="5d984-129">In the dialog header, the requisite headers must be included and the template class you created must be inherited.</span></span> <span data-ttu-id="5d984-130">您要在其中繼承的類別和事件處理常式必須具有向前宣告，才能實作為範本。</span><span class="sxs-lookup"><span data-stu-id="5d984-130">The class you're inheriting within and the event handlers must have forward declarations so that the template can be implemented.</span></span> <span data-ttu-id="5d984-131">下列程式碼範例顯示如何完成這項操作。</span><span class="sxs-lookup"><span data-stu-id="5d984-131">The following code example shows how this is done.</span></span>


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
> <span data-ttu-id="5d984-132">除非您已將類別命名為與範例相同，否則範本類型 **CMIC \_ TEST \_ EventsDlg** 將會不同。</span><span class="sxs-lookup"><span data-stu-id="5d984-132">The template type, **CMIC\_TEST\_EventsDlg**, will be different unless you have named your class the same as the example.</span></span>

 

## <a name="initialize-your-class-to-inherit-the-event-sinks"></a><span data-ttu-id="5d984-133">初始化您的類別，以繼承事件接收 (s) </span><span class="sxs-lookup"><span data-stu-id="5d984-133">Initialize your class to inherit the event sink(s)</span></span>

<span data-ttu-id="5d984-134">當您將類別設定為繼承自範本類別之後，您就可以設定它來處理事件。</span><span class="sxs-lookup"><span data-stu-id="5d984-134">Once you have set up your class to inherit from the template class, you are ready to set it up to handle events.</span></span> <span data-ttu-id="5d984-135">這會包含初始化類別以具有數學輸入控制項和呼叫類別的控制碼。</span><span class="sxs-lookup"><span data-stu-id="5d984-135">This will consist of initializing the class to have a handle to the math input control and the calling class.</span></span> <span data-ttu-id="5d984-136">此外，用來處理事件的數學輸入控制項必須傳送至 CMathInputControlEventHandler 範例類別所繼承的 DispEventAdvise 方法。</span><span class="sxs-lookup"><span data-stu-id="5d984-136">Additionally, the math input control to handle events from must be sent to the DispEventAdvise method that the CMathInputControlEventHandler example class inherits.</span></span> <span data-ttu-id="5d984-137">下列程式碼會從範例類別中的 OnInitDialog 方法呼叫，以執行這些動作。</span><span class="sxs-lookup"><span data-stu-id="5d984-137">The following code is called from the OnInitDialog method in the example class to perform these actions.</span></span>


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
> <span data-ttu-id="5d984-138">\_在此範例中，範本類型 CMIC TEST \_ EventsDlg 將會不同，除非您已將類別命名為與範例相同。</span><span class="sxs-lookup"><span data-stu-id="5d984-138">The template type, CMIC\_TEST\_EventsDlg in this example, will be different unless you have named your class the same as the example.</span></span>

 

 

 
