---
title: Rich Edit 函數
description: Rich Edit 函數
ms.assetid: 5e913cb6-d561-447f-b33e-9160a8f46cda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df1b74069b63220a07bfb1bd5e3f5a1ad99a6c6c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482454"
---
# <a name="rich-edit-functions"></a>Rich Edit 函數

## <a name="in-this-section"></a>本節內容




| 主題 | 描述 | 
|-------|-------------|
| <a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a><br /> | <a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a>函式是應用程式定義的回呼函式，可搭配<a href="em-setautocorrectproc.md"><strong>EM_SETAUTOCORRECTPROC</strong></a>訊息使用。<br /> | 
| <a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a><br /> | <a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a>函式是一種應用程式定義的回呼函式，與<a href="em-streamin.md"><strong>EM_STREAMIN</strong></a>和<a href="em-streamout.md"><strong>EM_STREAMOUT</strong></a>的訊息搭配使用。 它是用來將資料流程傳入或流出 rich edit 控制項。 <strong>EDITSTREAMCALLBACK</strong>型別定義此回呼函數的指標。 <em>EditStreamCallback</em> 是應用程式定義函數名稱的預留位置。 <br /> | 
| <a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a><br /> | <a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a>函式是搭配<a href="em-setwordbreakprocex.md"><strong>EM_SETWORDBREAKPROCEX</strong></a>訊息使用的應用程式定義回呼函數。 它會決定文字分隔的字元索引，或字元類別，以及指定文字中字元的字元類別和文字分隔旗標。 <strong>EDITWORDBREAKPROCEX</strong>型別定義此回呼函數的指標。 <em>EditWordBreakProcEx</em> 是應用程式定義函數名稱的預留位置。 <br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780353(v=vs.85)"><strong>GetMathAlphanumeric</strong></a><br /> | 抓取 Unicode 轉換格式 (UTF-16) -32 math 英數位元，其對應至指定的基本多語系平面 (BMP) 字元和數學樣式。 <br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780354(v=vs.85)"><strong>GetMathAlphanumericCode</strong></a><br /> | 抓取數學樣式以及垂直基本多語系平面 (BMP) 字元碼，對應至數學代理配對的指定尾端位元組。<br /> | 
| <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a><br /> | <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a>函式是搭配<a href="em-sethyphenateinfo.md"><strong>EM_SETHYPHENATEINFO</strong></a>訊息使用的應用程式定義回呼函數。 它會決定如何在 Microsoft Rich Edit 控制項中完成斷字。<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780443(v=vs.85)"><strong>MathBuildDown</strong></a><br /> | 將指定範圍內的內建數學、ruby 和其他内嵌物件轉譯成線性形式。<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780445(v=vs.85)"><strong>MathBuildUp</strong></a><br /> | 將範圍中的線性格式數學轉換成內建表單，或修改目前的內建表單。 <br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780446(v=vs.85)"><strong>MathTranslate</strong></a><br /> | 轉譯指定範圍內的數學字元。<br /> | 
| <a href="reextendedregisterclass.md"><strong>REExtendedRegisterClass</strong></a><br /> | 註冊兩個類別名稱（REListBox20W 和 RECombobox20W），可用來建立 Rich Edit listbox 或 combobox 視窗。 <br /><blockquote>[!Note]<br />適用于內部用途;不建議在應用程式中使用。 未來的版本可能不支援此功能。</blockquote><br /> | 




 

 

