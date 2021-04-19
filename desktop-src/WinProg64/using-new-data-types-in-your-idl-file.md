---
title: 在 IDL 檔案中使用新的資料類型
description: Basetsd .h 標頭檔會定義撰寫在32和64位 Windows 上執行之應用程式所需的新資料類型。
ms.assetid: 99a3904b-9120-4d1d-bd8c-1eb299bd6b27
keywords:
- Basetsd .h 標頭檔 64-位 Windows 程式設計
- IDL 檔案64位 Windows 程式設計中的資料類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ff1add2d70c99069911ac76ad168b7d31c3365f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967487"
---
# <a name="using-new-data-types-in-your-idl-file"></a>在 IDL 檔案中使用新的資料類型

Basetsd .h 標頭檔會定義撰寫在32和64位 Windows 上執行之應用程式所需的新資料類型。 若要在您的介面中使用這些資料類型，請將 Basetsd 匯入至 IDL 檔案。 請勿包含檔案， \# 或在編譯時期最後會有多個定義。

或者，您也可以在 IDL 檔案中包含或匯入 Basetsd .idl 檔。

如需將系統標頭檔新增至 IDL 檔案的詳細資訊，請參閱匯 [入檔案和型別程式庫](/windows/desktop/Midl/importing-files-and-type-libraries) 和匯 [入系統標頭檔](/windows/desktop/Midl/importing-system-header-files)。

 

 