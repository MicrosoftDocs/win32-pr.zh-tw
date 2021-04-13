---
title: WriteXmlSimpleExample
description: 此範例會寫入簡單的 xml 檔。
ms.assetid: 9af95856-cd17-414a-aa4c-6a9927acf81e
keywords:
- 適用于 Windows 的 WriteXmlSimpleExample Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5456d9a8d571e0ae669ec8f910c14dc9a417911
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300343"
---
# <a name="writexmlsimpleexample"></a>WriteXmlSimpleExample

此範例會寫入簡單的 xml 檔。

-   [WriteXmlSimple .cpp](#writexmlsimplecpp)
-   [Makefile](#makefile)

## <a name="writexmlsimplecpp"></a>WriteXmlSimple .cpp


```C++
//------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
//------------------------------------------------------------

#ifndef UNICODE
#define UNICODE
#endif
#include <windows.h>
#include <stdio.h>
#include <WebServices.h>

#pragma comment(lib, "WebServices.lib")

// Print out rich error info
void PrintError(HRESULT errorCode, WS_ERROR* error)
{
    wprintf(L"Failure: errorCode=0x%lx\n", errorCode);

    if (errorCode == E_INVALIDARG || errorCode == WS_E_INVALID_OPERATION)
    {
        // Correct use of the APIs should never generate these errors
        wprintf(L"The error was due to an invalid use of an API.  This is likely due to a bug in the program.\n");
        DebugBreak();
    }

    HRESULT hr = NOERROR;
    if (error != NULL)
    {
        ULONG errorCount;
        hr = WsGetErrorProperty(error, WS_ERROR_PROPERTY_STRING_COUNT, &errorCount, sizeof(errorCount));
        if (FAILED(hr))
        {
            goto Exit;
        }
        for (ULONG i = 0; i < errorCount; i++)
        {
            WS_STRING string;
            hr = WsGetErrorString(error, i, &string);
            if (FAILED(hr))
            {
                goto Exit;
            }
            wprintf(L"%.*s\n", string.length, string.chars);
        }
    }
Exit:
    if (FAILED(hr))
    {
        wprintf(L"Could not get error string (errorCode=0x%lx)\n", hr);
    }
}

WS_XML_STRING valueLocalName = WS_XML_STRING_VALUE("value");
WS_XML_STRING valueNs = WS_XML_STRING_VALUE("");

// Main entry point
int __cdecl wmain(int argc, __in_ecount(argc) wchar_t **argv)
{
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);
    
    HRESULT hr = NOERROR;
    WS_ERROR* error = NULL;
    WS_XML_WRITER* writer = NULL;
    
    // Create an error object for storing rich error information
    hr = WsCreateError(
        NULL, 
        0, 
        &error);
    if (FAILED(hr))
    {
        goto Exit;
    }
    
    // Create an XML writer
    hr = WsCreateWriter(
        NULL, 
        0, 
        &writer, 
        error);
    if (FAILED(hr))
    {
        goto Exit;
    }
    
    // Setup the output
    WS_XML_WRITER_BUFFER_OUTPUT bufferOutput;
    ZeroMemory(
        &bufferOutput, 
        sizeof(bufferOutput));
    
    bufferOutput.output.outputType = WS_XML_WRITER_OUTPUT_TYPE_BUFFER;
    
    // Setup the encoding
    WS_XML_WRITER_TEXT_ENCODING textEncoding;
    ZeroMemory(
        &textEncoding, 
        sizeof(textEncoding));
    
    textEncoding.encoding.encodingType = WS_XML_WRITER_ENCODING_TYPE_TEXT;
    textEncoding.charSet = WS_CHARSET_UTF16LE;
    
    // Setup the writer
    hr = WsSetOutput(
        writer, 
        &textEncoding.encoding, 
        &bufferOutput.output, 
        NULL, 
        0, 
        error);
    if (FAILED(hr))
    {
        goto Exit;
    }
    hr = WsWriteStartElement(
        writer, 
        NULL, 
        &valueLocalName, 
        &valueNs, 
        error);
    if (FAILED(hr))
    {
        goto Exit;
    }
    hr = WsWriteChars(
        writer, 
        L"Hello world.", 
        12, 
        error);
    if (FAILED(hr))
    {
        goto Exit;
    }
    hr = WsWriteEndElement(
        writer, 
        error);
    if (FAILED(hr))
    {
        goto Exit;
    }
    
    WS_BYTES bytes;
    hr = WsGetWriterProperty(
        writer, 
        WS_XML_WRITER_PROPERTY_BYTES, 
        &bytes, 
        sizeof(bytes), 
        error);
    if (FAILED(hr))
    {
        goto Exit;
    }
    wprintf(
        L"%.*s\n", 
        bytes.length / sizeof(WCHAR), 
        (WCHAR*)bytes.bytes);
Exit:
    if (FAILED(hr))
    {
        // Print out the error
        PrintError(hr, error);
    }
    fflush(
        stdout);
    
    if (writer != NULL)
    {
        WsFreeWriter(writer);
    }
    if (error != NULL)
    {
        WsFreeError(error);
    }
    fflush(stdout);
    return SUCCEEDED(hr) ? 0 : -1;
}

```



## <a name="makefile"></a>Makefile

``` syntax
#------------------------------------------------------------
# Copyright (C) Microsoft.  All rights reserved.
#------------------------------------------------------------

!include <Win32.Mak>

EXTRA_LIBS = WebServices.lib rpcrt4.lib

all: $(OUTDIR) $(OUTDIR)\WsWriteXmlSimple.exe

"$(OUTDIR)" :
    if not exist "$(OUTDIR)/$(NULL)" mkdir "$(OUTDIR)"
    
$(OUTDIR)\WriteXmlSimple.obj: WriteXmlSimple.cpp
    $(cc) $(cdebug) $(cflags) $(cvarsmt) /WX -I$(OUTDIR) /Fo"$(OUTDIR)\\" /Fd"$(OUTDIR)\\" WriteXmlSimple.cpp

$(OUTDIR)\WsWriteXmlSimple.exe: $(OUTDIR)\WriteXmlSimple.obj
    $(link) $(ldebug) $(conlflags) $(conlibsmt) $(EXTRA_LIBS) -out:$(OUTDIR)\WsWriteXmlSimple.exe $(OUTDIR)\WriteXmlSimple.obj /PDB:$(OUTDIR)\WsWriteXmlSimple.PDB

clean:
    $(CLEANUP)

```

 

 




