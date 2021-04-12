---
title: 使用多個執行緒撰寫的 WinSNMP 應用程式
description: Microsoft 的 WinSNMP 實行可確保某個進程的 WinSNMP 作業不會修改其他進程的 WinSNMP 設定。
ms.assetid: faa98704-f55f-4450-9f6e-d2bbbc7a50b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb6b7991968c5c5efafa898758c3c60cad1abb2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375928"
---
# <a name="writing-winsnmp-applications-with-multiple-threads"></a>使用多個執行緒撰寫的 WinSNMP 應用程式

Microsoft 的 WinSNMP 實行可確保某個進程的 WinSNMP 作業不會修改其他進程的 WinSNMP 設定。

具有多個執行緒的 WinSNMP 應用程式必須確保設定應用層級參數的 WinSNMP 作業具有安全線程。 設定應用層級參數的函數為 [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode) 和 [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode)。 這些函式會修改實體的設定和內容轉譯模式，以及重新傳輸模式。

如需詳細資訊，請參閱 [多執行緒](/windows/desktop/ProcThread/multiple-threads) 和 [執行緒安全性和存取權限](/windows/desktop/ProcThread/thread-security-and-access-rights)。

 

 