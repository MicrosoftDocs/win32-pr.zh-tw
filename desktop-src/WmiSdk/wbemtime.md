---
description: WBEMTime 類別可加速各種 Windows 和 ANSI C 執行時間時間格式之間的轉換。 如需詳細資訊，請參閱 WBEMTimeSpan 類別方法。
ms.assetid: b633bc8c-9d02-4bcf-8528-10773fb5ae7a
ms.tgt_platform: multiple
title: WBEMTime 類別 (WbemTime.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WBEMTime
api_type:
- COM
api_location:
- FrameDynOS.dll
- FrameDyn.dll
ms.openlocfilehash: 16b4e8933113386e877aec23313f74695b321f932c10f0e2730bcf5888675cc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553244"
---
# <a name="wbemtime-class"></a>WBEMTime 類別

\[**WBEMTime** 類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。 [MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]

**WBEMTime** 類別可加速各種 Windows 和 ANSI C 執行時間時間格式之間的轉換。 如需詳細資訊，請參閱 [**WBEMTimeSpan 類別方法**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan)。

## <a name="members"></a>成員

**WBEMTime** 類別具有下列類型的成員：

-   [建構函式](#constructors)
-   [方法](#methods)

### <a name="constructors"></a>建構函式

**WBEMTime** 類別具有這些函式。



| 建構函式                           | 描述                                                                                                   |
|:--------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**WBEMTime**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-wbemtime(constbstr)) | 可加速各種 Windows 和 ANSI C 執行時間時間格式之間轉換的函式。<br/> |



 

### <a name="methods"></a>方法

**WBEMTime** 類別有這些方法。



| 方法                                                           | 描述                                                                                                                            |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**清除**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-clear)                                  | 將 **WBEMTime** 物件中的時間設定為無效時間。<br/>                                                                |
| [**GetBSTR**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getbstr)                              | 以 **BSTR** 值呈現時間。<br/>                                                                                      |
| [**GetDMTF**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getdmtf)                              | 以 CIM datetime 格式取得 **BSTR** 值的時間。<br/>                                                                   |
| [**GetDMTFNonNtfs**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getdmtfnonntfs)                | 取得以 FAT 或 [日期和時間格式](date-and-time-format.md) 為基礎的 DMTF 日期（UTC 未知）。<br/> |
| [**GetFILETIME**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getfiletime)                      | 取得做為 MFC **FILETIME** 結構的時間。<br/>                                                                             |
| [**GetLocalOffsetForDate**](/previous-versions/windows/desktop/legacy/aa394049(v=vs.85)) | 多載。 傳回引數中所提供時間的時差，以分鐘為單位 (+ 或-) 。<br/>         |
| [**GetStructtm**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getstructtm)                      | 取得以 ANSI C 執行時間 **結構 tm** 結構為時間的時間。<br/>                                                                |
| [**GetSYSTEMTIME**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getsystemtime)                  | 取得做為 MFC **SYSTEMTIME** 結構的時間。<br/>                                                                           |
| [**GetTime**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-gettime)                              | 取得以64位整數為單位的時間。<br/>                                                                                          |
| [**Gettime \_ t**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-gettime_t)                         | 取得 ANSI C 執行時間時間 \_ t 變數的時間。<br/>                                                                       |
| [**>isok**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-isok)                                    | 指出 **WBEMTime** 物件是否代表有效的時間。<br/>                                                          |
| [**SetDMTF**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-setdmtf)                              | 以 CIM datetime 格式設定 **WBEMTime** 物件中的時間。<br/>                                                            |



 

## <a name="wbemtime-overloaded-operators"></a>WBEMTime 多載運算子

**WBEMTime** 物件定義了下列多載運算子。



| WBEMTime 多載運算子                                                                                                                                                                                                                                                                                                                                                                                                                                        | 描述                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**運算子 =**](/previous-versions/windows/desktop/legacy/aa394050(v=vs.85))                                                                                                                                                                                                                                                                                                                                                                                                                       | *指派* 運算子可加速各種 Windows 和 ANSI C 執行時間時間格式之間的轉換。                           |
| [**運算子 +**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-add)                                                                                                                                                                                                                                                                                                                                                                                                                         | *加法* 運算子會以時間範圍遞增物件的時間。 結果會在新的 **WBEMTime** 物件中傳回。              |
| [**運算子 + =**](/windows/win32/api/directxmath/nf-directxmath-operator-add-assign)                                                                                                                                                                                                                                                                                                                                                                                                                  | *Add 和 assign* 運算子會以時間範圍遞增物件的時間。                                                             |
| [**運算子**](/previous-versions/windows/desktop/legacy/aa394051(v=vs.85))                                                                                                                                                                                                                                                                                                                                                                                                                       | *減法* 運算子會將物件的時間遞減為另一個物件的時間。 結果會在新的 **WBEMTime** 物件中傳回。 |
| [**operator-=**](/windows/win32/api/directxmath/nf-directxmath-operator-sub-assign)                                                                                                                                                                                                                                                                                                                                                                                                                 | *減號和賦值* 運算子會將物件的時間遞減一段時間。                                                        |
| [**operator = =**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-equal-equal-to)[**運算子！ =**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-not-equal-to)<br/> [**運算子 >**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than)<br/> [**運算子 >=**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than-equal-to)<br/> [**運算子 <**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-less-than)<br/> [**運算子 <=**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-less-than-equal-to)<br/> | 比較運算子會比較兩個 **WBEMTime** 物件。                                                                            |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                                                                                      |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                                                                                |
| 標頭<br/>                   | <dl> <dt>WbemTime。h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll;</dt><dt>FrameDyn.dll</dt> </dl> |



 

