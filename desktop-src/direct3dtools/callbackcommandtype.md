---
description: <span id="vspixengine.callbackcommandtype"></span>CallbackCommandType 列舉-用來在 capture 引擎和主機 (（例如 Visual Studio 圖形診斷) ）之間進行通訊的列舉。
MS-HAID: vspixengine.CallbackCommandType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: CallbackCommandType 列舉
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 78E0CD6C-5264-4F66-BAB9-20DC9C0C1EC1
api_name:
- CallbackCommandType
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 85e1b7d396d125add00824e9b7c94086e0da6be2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090126"
---
# <a name="span-idvspixenginecallbackcommandtypespancallbackcommandtype-enumeration"></a><span id="vspixengine.callbackcommandtype"></span>CallbackCommandType 列舉

用來在 capture 引擎和主機 (（例如 Visual Studio 圖形診斷) ）之間進行通訊的列舉。

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>常數

<span id="BeginCommunicationCallback"></span><span id="begincommunicationcallback"></span><span id="BEGINCOMMUNICATIONCALLBACK"></span>**BeginCommunicationCallback**  
來自 BeginCommunication 的結果。

<span id="ErrorListCallback"></span><span id="errorlistcallback"></span><span id="ERRORLISTCALLBACK"></span>**ErrorListCallback**  
錯誤。

<span id="WarningListCallback"></span><span id="warninglistcallback"></span><span id="WARNINGLISTCALLBACK"></span>**WarningListCallback**  
警告：

<span id="MessagesCallback"></span><span id="messagescallback"></span><span id="MESSAGESCALLBACK"></span>**MessagesCallback**  
訊息。

<span id="RunExperimentCallback"></span><span id="runexperimentcallback"></span><span id="RUNEXPERIMENTCALLBACK"></span>**RunExperimentCallback**  
來自 RunExperiment 的結果。

<span id="RunActionCallback"></span><span id="runactioncallback"></span><span id="RUNACTIONCALLBACK"></span>**RunActionCallback**  
來自 RunAction 的結果。

<span id="NewFramesCallback"></span><span id="newframescallback"></span><span id="NEWFRAMESCALLBACK"></span>**NewFramesCallback**  
值，這個值表示當已捕捉新框架並可供顯示時，所要呼叫的回呼。

<span id="BeginCommunicationCallbackLegacy"></span><span id="begincommunicationcallbacklegacy"></span><span id="BEGINCOMMUNICATIONCALLBACKLEGACY"></span>**BeginCommunicationCallbackLegacy**  
在 Windows 7 和 Windows 8 上使用的舊版 BeginCommunication 結果。

<span id="RunExperimentStatusCallback"></span><span id="runexperimentstatuscallback"></span><span id="RUNEXPERIMENTSTATUSCALLBACK"></span>**RunExperimentStatusCallback**  
來自 RunExperiementProgress 的結果。

## <a name="requirements"></a>規格需求

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

 

 



