---
description: 此介面的實作為使用 DirectShow SDK 的範例程式碼來提供。
ms.assetid: a18fc6b6-f37e-4c87-9150-0504333d33c2
title: IMpeg2PsiParser 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser
api_type:
- COM
api_location: ''
ms.openlocfilehash: 51f0f3373c67da75c50ecc2f6bc234e0351f5dc3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970494"
---
# <a name="impeg2psiparser-interface"></a>IMpeg2PsiParser 介面

此介面的實作為使用 DirectShow SDK 的範例程式碼來提供。 這不是支援的 DirectShow API。

此 `IMpeg2PsiParser` 介面會從 psi 剖析器篩選器中取出程式特定資訊 (psi) ，此篩選器會在 DIRECTSHOW SDK 中以範例篩選器的形式提供。 應用程式可以使用此篩選器，將程式識別碼對應至 MPEG-2 信號篩選器上的 (Pid) 。

## <a name="members"></a>成員

**IMpeg2PsiParser** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IMpeg2PsiParser** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IMpeg2PsiParser** 介面具有這些方法。



| 方法                                                                             | 描述                                                                               |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**FindRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd407137(v=vs.85))         | 根據程式編號，找出程式的對應表 (PMT) PID。<br/> |
| [**GetCountOfElementaryStreams**](impeg2psiparser-getcountofelementarystreams.md) | 抓取指定程式中的基本資料流程數目。<br/>             |
| [**GetCountOfPrograms**](impeg2psiparser-getcountofprograms.md)                   | 捕獲傳輸資料流程中的程式數目。<br/>                      |
| [**GetPatVersionNumber**](impeg2psiparser-getpatversionnumber.md)                 | \_從程式關聯資料表中，抓取 (PAT) 的 [版本號碼] 欄位。<br/>  |
| [**GetPmtVersionNumber**](impeg2psiparser-getpmtversionnumber.md)                 | \_從指定的 PMT 抓取版本號碼欄位。<br/>                      |
| [**GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85))           | 抓取程式中指定之基本資料流程的 PID 指派。<br/>   |
| [**GetRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd376624(v=vs.85))           | 抓取指定之 PMT 的 PID 指派。<br/>                              |
| [**GetRecordProgramNumber**](impeg2psiparser-getrecordprogramnumber.md)           | 抓取指定程式的程式編號。<br/>                          |
| [**GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85))                 | 抓取程式中指定之基本資料流程的資料流程類型。<br/>      |
| [**GetTransportStreamId**](impeg2psiparser-gettransportstreamid.md)               | \_從 PAT 抓取傳輸資料流程 \_ 識別碼欄位。<br/>                        |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[PSI 剖析器篩選範例](psi-parser-filter-sample.md)
</dt> </dl>

 

 
