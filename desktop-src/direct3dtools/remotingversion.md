---
description: 列舉，用來指出正在使用的遠端 protocul 版本。
MS-HAID: vspixengine.REMOTINGVERSION
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: REMOTINGVERSION 列舉
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 598E9586-05FF-4889-BBAF-44814EEF203A
api_name:
- REMOTINGVERSION
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a813453f9b5d1a89525e5b67cc22659281d04cb5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317612"
---
# <a name="span-idvspixengineremotingversionspanremotingversion-enumeration"></a><span id="vspixengine.remotingversion"></span>REMOTINGVERSION 列舉

列舉，用來指出正在使用的遠端 protocul 版本。

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>常數

<span id="REMOTING_DEV12"></span><span id="remoting_dev12"></span>**遠端 \_ DEV12**  
指出正在使用 Visual Studio 2013 RTM 遠端處理通訊協定的值。

<span id="REMOTING_DEV12_UPDATE_1"></span><span id="remoting_dev12_update_1"></span>**遠端 \_ DEV12 \_ UPDATE \_ 1**  
指出正在使用 Visual Studio 2013 Update 1 遠端處理通訊協定的值。

<span id="REMOTING_DEV12_UPDATE_4"></span><span id="remoting_dev12_update_4"></span>**遠端 \_ DEV12 \_ 更新 \_ 4**  
指出正在使用 Visual Studio 2013 Update 4 遠端處理通訊協定的值。

<span id="REMOTING_DEV14"></span><span id="remoting_dev14"></span>**遠端 \_ DEV14**  
指出正在使用 Visual Studio 2015 RTM 遠端處理通訊協定的值。

<span id="REMOTING_WIN10"></span><span id="remoting_win10"></span>**遠端 \_ WIN10**  
值，指出 Windows 10 遠端處理通訊協定正在使用中 (從 Windows 10 開始，圖形診斷是作業系統元件) 

<span id="REMOTING_WIN10_JAN_2015"></span><span id="remoting_win10_jan_2015"></span>**遠端 \_ WIN10 \_ JAN \_ 2015**  
值，表示正在使用 Windows 10 (2015 年1月) 遠端處理通訊協定。

<span id="REMOTING_WIN10_JAN_2015_1"></span><span id="remoting_win10_jan_2015_1"></span>**遠端 \_ WIN10 \_ JAN \_ 2015 \_ 1**  
值，表示使用的是 Windows 10 (2015 年1月，) 遠端處理通訊協定正在使用中。

<span id="REMOTING_WIN10_JAN_2015_2"></span><span id="remoting_win10_jan_2015_2"></span>**遠端 \_ WIN10 \_ JAN \_ 2015 \_ 2**  
值，表示正在使用 Windows 10 (2015 年1月) 遠端處理通訊協定。 此版本的通訊協定引進了視覺效果視覺化資源的要求。

<span id="REMOTING_WIN10_JAN_2015_3"></span><span id="remoting_win10_jan_2015_3"></span>**遠端 \_ WIN10 \_ JAN \_ 2015 \_ 3**  
值，表示正在使用 Windows 10 (2015 年1月) 遠端處理通訊協定。 此版本的通訊協定引進了 IPixEngine7，現在已被取代，可檢查介面版本的支援。

<span id="REMOTING_IPIXENGINE7_VERSION_CHECKING"></span><span id="remoting_ipixengine7_version_checking"></span>**遠端 \_ IPIXENGINE7 \_ 版本 \_ 檢查**  
值，表示使用的是 Windows 10 (2015 年1月，) 遠端處理通訊協定正在使用中。 此版本的通訊協定會從依賴 REMOTINGVERSION 到協調通訊協定功能而離開。 介面 GUID 現在會在非公用 int 變更時變更

<span id="REMOTING_WIN10_FEB_2015_1"></span><span id="remoting_win10_feb_2015_1"></span>**遠端 \_ WIN10 在 \_ 2015 年2月 \_ \_ 1 日**  
值，表示使用的是 Windows 10 (2015 年1月，) 遠端處理通訊協定正在使用中。 此版本的通訊協定會以唯一的固定識別碼引進摘要資訊屬性。

<span id="REMOTING_WIN10_2015_03_00"></span><span id="remoting_win10_2015_03_00"></span>**遠端處理 \_ WIN10 \_ 2015 \_ 03 \_ 00**  
值，表示使用的是 Windows 10 (2015 年1月，) 遠端處理通訊協定正在使用中。 此版本的通訊協定引進了 DirectX11 狀態視窗的支援。

<span id="REMOTING_LATES"></span><span id="remoting_lates"></span>**遠端 \_ LATES**  
值，表示正在使用最新的遠端處理通訊協定。

## <a name="requirements"></a>規格需求

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

 

 



