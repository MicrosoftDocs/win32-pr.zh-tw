---
title: 轉換 Unicode 和 ANSI 字串
description: Microsoft Active Accessibility 使用 BSTR 資料類型所定義的 Unicode 字串。
ms.assetid: 47f525fe-6d18-43b9-a706-e49afa796830
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fa26813c61be0a3959593f370016cfce0211ea9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315784"
---
# <a name="converting-unicode-and-ansi-strings"></a>轉換 Unicode 和 ANSI 字串

Microsoft Active Accessibility 使用 **BSTR** 資料類型所定義的 Unicode 字串。 如果您的應用程式不使用 Unicode 字串，或如果您想要轉換特定 API 呼叫的字串，請使用 [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) 和 [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) Microsoft Win32 函數來執行必要的轉換。

使用 [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) 將 Unicode 字串轉換為 ANSI 字串。 [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)函數會將 ANSI 字串轉換成 Unicode 字串。

使用 [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) 和 [**SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) 來配置及釋放 **BSTR** 資料類型。

如需這些字串函數的詳細資訊，請參閱 Windows 軟體開發套件 (SDK) 的參考。

 

 