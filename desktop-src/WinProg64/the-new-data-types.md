---
title: 新的資料類型
description: 針對64位的 Windows 固定精確度資料類型、指標精確度型別和特定指標精確度型別引進了三種資料類型類別。
ms.assetid: 016977d4-e7bf-463e-9755-7ef13f16e9e5
keywords:
- 64位 Windows 程式設計指南64位 Windows 程式設計，資料類型
- 資料類型64位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6cf5960b5344da1d459d12dee96a2f67f2cfbc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316216"
---
# <a name="the-new-data-types"></a>新的資料類型

針對64位 Windows 引進了三種資料類型：固定精確度資料類型、指標精確度類型，以及特定指標精確度類型。 這些類型已新增至開發環境，可讓開發人員為64位 Windows 做好準備。 這些類型衍生自基本的 C 語言整數和 long 類型。 因此，您可以在32位 Windows 上編譯並測試的程式碼中使用這些資料類型，然後在以64位 Windows 為目標時，使用64位編譯器進行重新編譯。

即使是以32位 Windows 為目標的應用程式，採用這些新的資料類型可讓您的程式碼更健全。 若要使用這些資料類型，您必須掃描程式碼中是否有潛在的不安全指標使用方式、多型和資料定義。 例如，當變數屬於 **ULONG \_ PTR** 類型時，就會清除它將用於轉換算數運算或多型的指標。 使用較舊的資料類型，並不可能直接指出這類使用量。  (您可以使用衍生的型別命名或匈牙利文標記法來間接完成這項作業，但是這兩種技術很容易發生錯誤。 ) 

所有這些資料類型都是在 BaseTsd 中宣告。 如需詳細資訊（包括這些資料類型的定義），請參閱 [Windows 資料類型](/windows/desktop/WinProg/windows-data-types)。

## <a name="fixed-precision"></a>固定有效位數

固定精確度的資料類型在32和64位的視窗中都是相同的長度。 為了協助您記住這一點，其精確度是資料類型名稱的一部分。 以下是固定精確度的資料類型。



| 詞彙                                                                       | 描述                        |
|----------------------------------------------------------------------------|------------------------------------|
| <span id="DWORD32"></span><span id="dword32"></span>**DWORD32**<br/> | 32 位元不帶正負號的整數<br/> |
| <span id="DWORD64"></span><span id="dword64"></span>**DWORD64**<br/> | 64 位元不帶正負號的整數<br/> |
| <span id="INT32"></span><span id="int32"></span>**時會**<br/>       | 32 位元帶正負號的整數<br/>   |
| <span id="INT64"></span><span id="int64"></span>**INT64**<br/>       | 64 位元帶正負號的整數<br/>   |
| <span id="LONG32"></span><span id="long32"></span>**LONG32**<br/>    | 32 位元帶正負號的整數<br/>   |
| <span id="LONG64"></span><span id="long64"></span>**LONG64**<br/>    | 64 位元帶正負號的整數<br/>   |
| <span id="UINT32"></span><span id="uint32"></span>**UINT32**<br/>    | 不帶正負號的 **INT32**<br/>      |
| <span id="UINT64"></span><span id="uint64"></span>**UINT64**<br/>    | 未簽署的 **INT64**<br/>      |
| <span id="ULONG32"></span><span id="ulong32"></span>**ULONG32**<br/> | 未簽署的 **LONG32**<br/>     |
| <span id="ULONG64"></span><span id="ulong64"></span>**ULONG64**<br/> | 未簽署的 **LONG64**<br/>     |



 

## <a name="pointer-precision"></a>指標精確度

隨著指標精確度的變更 (也就是，當32位 Windows 上的32位和64位 Windows) 的64位時，指標精確度資料類型會據以反映精確度。 因此，在執行指標算術時，可以安全地將指標轉換成下列其中一種類型：如果指標有效位數是64位，則類型為64位。 計數類型也會反映指標可參考的大小上限。 以下是指標精確度和計數類型。



| 詞彙                                                                              | 描述                                                                                                                      |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span id="DWORD_PTR"></span><span id="dword_ptr"></span>**DWORD \_ PTR**<br/> | 指標有效位數不帶正負號的 long 類型。<br/>                                                                             |
| <span id="HALF_PTR"></span><span id="half_ptr"></span>**半 \_ PTR**<br/>    | 指標的一半大小。 在包含指標和兩個小型欄位的結構中使用。<br/>                      |
| <span id="INT_PTR"></span><span id="int_ptr"></span>**INT \_ PTR**<br/>       | 指標有效位數的帶正負號整數類型。<br/>                                                                            |
| <span id="LONG_PTR"></span><span id="long_ptr"></span>**長 \_ PTR**<br/>    | 指標有效位數的帶正負號的 long 類型。<br/>                                                                               |
| <span id="SIZE_T"></span><span id="size_t"></span>**大小 \_ T**<br/>          | 指標可以參考的最大位元組數目。 用於必須橫跨指標完整範圍的計數。<br/> |
| <span id="SSIZE_T"></span><span id="ssize_t"></span>**SSIZE \_ T**<br/>       | 帶正負 **號的大小 \_ T**。<br/>                                                                                                   |
| <span id="UHALF_PTR"></span><span id="uhalf_ptr"></span>**UHALF \_ PTR**<br/> | 不帶正負號的 **半 \_ PTR**。<br/>                                                                                               |
| <span id="UINT_PTR"></span><span id="uint_ptr"></span>**UINT \_ PTR**<br/>    | 不帶正負號的 **INT \_ PTR**。<br/>                                                                                                |
| <span id="ULONG_PTR"></span><span id="ulong_ptr"></span>**ULONG \_ PTR**<br/> | 不帶正負號的 **長 \_ 指標**。<br/>                                                                                               |



 

## <a name="specific-pointer-precision-types"></a>特定的 Pointer-Precision 類型

下列新指標類型會明確地調整指標的大小。 在64位程式碼中使用指標時請務必小心：如果您使用32位類型宣告指標，作業系統會藉由截斷64位指標來建立指標。  (64 位 Windows 上的所有指標都是64位。 ) 



| 詞彙                                                                                 | 描述                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="POINTER_32"></span><span id="pointer_32"></span>**指標 \_ 32**<br/> | 32位指標。 在32位的 Windows 上，這是原生指標。 在64位的 Windows 上，這是截斷的64位指標。<br/>                                                                                       |
| <span id="POINTER_64"></span><span id="pointer_64"></span>**指標 \_ 64**<br/> | 64位指標。 在64位的 Windows 上，這是原生指標。 在32位的 Windows 上，這是一個帶正負號的32位指標。 <br/> 請注意，假設高指標位的狀態並不安全。<br/> |



 

 

